```
> .\support\JetBrains.ReSharper.CommandLineTools.2019.3.1\cleanupcode.exe --profile=Hook .\IndexError.sln --trace
JetBrains Cleanup Code 2019.3.1
Running in 64-bit mode, .NET runtime 4.0.30319.42000 under Microsoft Windows NT 10.0.17763.0
Using toolset version 16.0 from "C:\Program Files\dotnet\sdk\3.0.100"
Configuration: Debug, Platform: Any CPU
Cleanup profile is specified. 'Hook' profile will be used to run cleanup
<OutputSolution>\OutputDefinition.cs
<OutputSolution>\OutputDefinition.cs - Applying code style, Processing redundancies
<OutputSolution>\OutputDefinition.cs - Formatting
<OutputSolution>\OutputDefinition.cs - Indenting
<OutputSolution>\OutputDefinition.cs - Formatting
<OutputSolution>\OutputDefinition.cs - Making blank lines
<OutputSolution>\OutputDefinition.cs - Aligning in columns
<OutputSolution>\OutputDefinition.cs - Indenting
<OutputSolution>\OutputDefinition.cs - Formatting
<OutputSolution>\OutputDefinition.cs - Making blank lines
<OutputSolution>\OutputDefinition.cs - Aligning in columns
Index should be non-negative and less than Count Parameter name: index

--- EXCEPTION #1/2 [ArgumentOutOfRangeException]
Message = "Index should be non-negative and less than Count"
ExceptionPath = Root.InnerException
ClassName = System.ArgumentOutOfRangeException
Data.ThreadLocalDebugInfo = "Code Cleanup"
HResult = COR_E_ARGUMENTOUTOFRANGE=80131502
Source = JetBrains.Platform.Core
ParamName = index
StackTraceString = "
  at JetBrains.Util.DataStructures.Collections.FixedList.FixedListBase`1.ThrowOutOfRange()
     at JetBrains.Util.DataStructures.Collections.FixedList.FixedListBase`1.Two.get_Item(Int32 index)
     at JetBrains.ReSharper.Psi.Xml.XmlDocComments.DocCommentXmlPsiBase`1.ComputeRangesMap()
     at JetBrains.ReSharper.Psi.Xml.XmlDocComments.DocCommentXmlPsiBase`1.GetDocToXmlRangesMap()
     at JetBrains.ReSharper.Psi.Xml.XmlDocComments.DocCommentXmlPsiBase`1.ToDocComment(TreeOffset offset, Int32& rangeIndex)
     at JetBrains.ReSharper.Psi.Xml.XmlDocComments.DocCommentXmlPsiBase`1.GeneratedToOriginal(TreeTextRange generatedRange)
     at JetBrains.ReSharper.Psi.Tree.FileExtensions.GetDocumentRange(IFile file, TreeTextRange range)
     at JetBrains.ReSharper.Psi.Impl.CodeStyle.CodeFormattingContext..ctor(ICodeFormatterImpl codeFormatter, ITreeNode firstNode, ITreeNode lastNode, CodeFormatProfile profile,
IFormatterDebugInfoLogger debugInfoLogger, AdditionalFormatterParameters parameters)
     at JetBrains.ReSharper.Psi.Xml.Impl.CodeStyle.XmlCodeFormattingContext..ctor(ICodeFormatterImpl codeFormatter, ITreeNode firstNode, ITreeNode lastNode, FmtSettings`1 format
tingSettings, CodeFormatProfile profile, IFormatterDebugInfoLogger debugInfoLogger, AdditionalFormatterParameters parameters)
     at JetBrains.ReSharper.Psi.Xml.Impl.CodeStyle.XmlCodeFormatter.CreateFormatterContext(CodeFormatProfile profile, ITreeNode firstNode, ITreeNode lastNode, AdditionalFormatte
rParameters parameters, ICustomFormatterInfoProvider provider)
     at JetBrains.ReSharper.Psi.Xml.Impl.CodeStyle.XmlCodeFormatter.Format(ITreeNode firstElement, ITreeNode lastElement, CodeFormatProfile profile, AdditionalFormatterParameter
s parameters)
     at JetBrains.ReSharper.Psi.Impl.CodeStyle.CodeFormatterBase`1.FormatFile(IFile fileNode, CodeFormatProfile profile, AdditionalFormatterParameters parameters)
     at JetBrains.ReSharper.Psi.Xml.Impl.CodeStyle.XmlDocFormatterImplHelper.FormatDocComment[TXmlPsi,TCommentNode](IDocCommentBlockWithPsi`2 node)
     at JetBrains.ReSharper.Feature.Services.CSharp.CodeCleanup.ReformatCode.<>c__DisplayClass10_0.<Process>b__0()
     at JetBrains.ReSharper.Psi.Transactions.PsiTransactions.Execute(String commandName, Action handler)
"

--- Outer ---

--- EXCEPTION #2/2 [LoggerException]
Message = "
  Index should be non-negative and less than Count
  Parameter name: index
"
ExceptionPath = Root
ClassName = JetBrains.Util.LoggerException
InnerException = "Exception #1 at Root.InnerException"
HResult = COR_E_APPLICATION=80131600
StackTraceString = "
  at JetBrains.Util.LoggerBase.Log(LoggingLevel level, String message, Exception ex)
     at JetBrains.Util.Logging.Logger.LogException(Exception ex)
     at JetBrains.ReSharper.Psi.Transactions.PsiTransactions.Execute(String commandName, Action handler)
     at JetBrains.ReSharper.Feature.Services.CodeCleanup.CodeCleanup.Run(IPsiSourceFile sourceFile, DocumentRange range, CodeCleanupProfile profile, IProgressIndicator progressI
ndicator)
     at JetBrains.ReSharper.Feature.Services.CodeCleanup.CodeCleanupEx.Run(CodeCleanup that, IList`1 files, CodeCleanupProfile profile, ISolution solution, IProgressIndicator pr
ogressIndicator)
     at JetBrains.ReSharper.Features.Altering.CodeCleanup.CodeCleanupRunner.<>c__DisplayClass1_1.<CleanupFiles>b__0(IProgressIndicator progress)
     at JetBrains.ReSharperAutomationTools.CommandLine.Common.Console.BatchTool.Progress.ToolTaskExecutor.ExecuteTask(String taskName, TaskCancelable cancelable, Action`1 task)
     at JetBrains.ReSharper.Features.Altering.CodeCleanup.CodeCleanupRunner.CleanupFiles(ICodeCleanupFilesProvider cleanupFilesCollector, CodeCleanupProfile cleanupProfile)
     at JetBrains.Application.Threading.IShellLocksEx.ExecuteWithReadLock(IShellLocks th?s, Action F)
     at JetBrains.Threading.ReentrancyGuard.Execute(String name, Action action)
     at JetBrains.Threading.ReentrancyGuard.TryExecute(String name, Action action)
     at JetBrains.Threading.ReentrancyGuardEx.ExecuteOrQueue(ReentrancyGuard th?s, Lifetime lifetime, String name, Action F, TaskPriority priority)
     at JetBrains.Application.Threading.IThreadingEx.ExecuteOrQueue(IThreading th?s, Lifetime lifetime, String name, Action action, TaskPriority priority)
     at JetBrains.Application.Threading.IShellLocksEx.ExecuteOrQueueReadLock(IShellLocks th?s, Lifetime lifetime, String name, Action F, TaskPriority priority)
     at JetBrains.CommandLine.CleanupCode.Unattended.CodeEditing.CleanupCodeLauncher.Run()
     at JetBrains.CommandLine.CleanupCode.Unattended.ConsoleCodeEditing.CleanupCodeProductMain.Main(Lifetime lifetime, IThreading invocator, IComponentContainer container, IShel
lLocks shellLocks, ILogger logger, ICleanupCodeSettings settings, IProductCommandLineArguments argumentsRaw)
     at System.RuntimeMethodHandle.InvokeMethod(Object target, Object[] arguments, Signature sig, Boolean constructor)
     at System.Reflection.RuntimeMethodInfo.UnsafeInvokeInternal(Object obj, Object[] parameters, Object[] arguments)
     at System.Reflection.RuntimeMethodInfo.Invoke(Object obj, BindingFlags invokeAttr, Binder binder, Object[] parameters, CultureInfo culture)
     at JetBrains.Application.Environment.RunsPublicStaticIntMain.<>c__DisplayClass0_0.<.ctor>b__0()
     at JetBrains.Util.Logging.Logger.Catch(Action action)
     at JetBrains.Threading.JetDispatcher.Closure.Execute()
     at JetBrains.Util.Concurrency.WinJetDispatcher.ProcessQueue(Int32 nMinBucket)
     at System.Windows.Threading.DispatcherOperation.InvokeDelegateCore()
     at System.Windows.Threading.DispatcherOperation.InvokeImpl()
     at MS.Internal.CulturePreservingExecutionContext.CallbackWrapper(Object obj)
     at System.Threading.ExecutionContext.RunInternal(ExecutionContext executionContext, ContextCallback callback, Object state, Boolean preserveSyncCtx)
     at System.Threading.ExecutionContext.Run(ExecutionContext executionContext, ContextCallback callback, Object state, Boolean preserveSyncCtx)
     at System.Threading.ExecutionContext.Run(ExecutionContext executionContext, ContextCallback callback, Object state)
     at MS.Internal.CulturePreservingExecutionContext.Run(CulturePreservingExecutionContext executionContext, ContextCallback callback, Object state)
     at System.Windows.Threading.DispatcherOperation.Invoke()
     at System.Windows.Threading.Dispatcher.ProcessQueue()
     at System.Windows.Threading.Dispatcher.WndProcHook(IntPtr hwnd, Int32 msg, IntPtr wParam, IntPtr lParam, Boolean& handled)
     at MS.Win32.HwndWrapper.WndProc(IntPtr hwnd, Int32 msg, IntPtr wParam, IntPtr lParam, Boolean& handled)
     at MS.Win32.HwndSubclass.DispatcherCallbackOperation(Object o)
     at System.Windows.Threading.ExceptionWrapper.InternalRealCall(Delegate callback, Object args, Int32 numArgs)
     at System.Windows.Threading.ExceptionWrapper.TryCatchWhen(Object source, Delegate callback, Object args, Int32 numArgs, Delegate catchHandler)
     at System.Windows.Threading.Dispatcher.LegacyInvokeImpl(DispatcherPriority priority, TimeSpan timeout, Delegate method, Object args, Int32 numArgs)
     at MS.Win32.HwndSubclass.SubclassWndProc(IntPtr hwnd, Int32 msg, IntPtr wParam, IntPtr lParam)
     at MS.Win32.UnsafeNativeMethods.DispatchMessage(MSG& msg)
     at MS.Win32.UnsafeNativeMethods.DispatchMessage(MSG& msg)
     at System.Windows.Threading.Dispatcher.PushFrameImpl(DispatcherFrame frame)
     at JetBrains.Application.Environment.IJetHostEx.<>c__DisplayClass2_0.<RunHostMessageLoop>b__0(Lifetime lifetime)
     at JetBrains.Lifetimes.Lifetime.Using(Action`1 action)
     at JetBrains.Application.Environment.IJetHostEx.RunHostMessageLoop(IComponentContainer containerEnv)
     at JetBrains.Application.Environment.HostParameters.JetHostParametersCaller.RunMainLoop(ComponentContainer containerEnv)
     at JetBrains.Application.Environment.JetEnvironment.InternalRun(JetHostParametersCaller host, ComponentContainer containerEnv)
     at JetBrains.Application.Environment.JetEnvironment.CreateAndRun(Full hostparams)
     at JetBrains.ReSharperAutomationTools.CommandLine.Common.Application.CommandLineProgram.Main(Assembly assembly, Type environmentZoneType, HostInfo hostInfo, ICommandLinePro
ductInfo productInfo, String[] args, IJetHostMixin[] mixins)
     at JetBrains.ReSharperAutomationTools.CommandLine.Common.Application.CommandLineProgram.Run[TZone,TProductInfo](String productHostShortName, String[] args)
     at JetBrains.CommandLine.CleanupCode.CleanupCodeProgram.Main(String[] args)
"
```