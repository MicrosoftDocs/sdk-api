---
UID: NF:winbase.OperationStart
title: OperationStart function
author: windows-sdk-content
description: Notifies the system that the application is about to start an operation.
old-location: oprec\operationstart.htm
old-project: oprec
ms.assetid: 3E67057E-D09F-48BA-A95A-5D00F4783D9C
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: OperationStart, OperationStart function [Operation Recorder], oprec.operationstart, winbase/OperationStart
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - OperationStart
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# OperationStart function


## -description


Notifies the system that the application is about to start an operation.

 If an application calls <b>OperationStart</b> with a valid <a href="https://msdn.microsoft.com/D5446D23-DBB5-4EB8-97E4-590537A33193">OPERATION_ID</a> value, the system records the specified operation’s file access patterns until <a href="https://msdn.microsoft.com/73C6FBDD-BB4A-46A5-8E39-7862A1938F47">OperationEnd</a> is called for the same operation ID. This record is stored in a <i>filename.pf</i> prefetch file. Every call to <b>OperationStart</b> must be followed by a call to <b>OperationEnd</b>, otherwise the operation's record is discarded after 10 seconds.


If an application calls <b>OperationStart</b> for an operation ID for which a prefetch file exists, the system loads the operation's files into memory prior to running the operation. The recording process remains the same and the system updates the appropriate <i>filename.pf</i> prefetch file. 


## -parameters




### -param OperationStartParams

TBD




#### - OperationParams [in]

An <a href="https://msdn.microsoft.com/51AE0017-2CDE-4BCD-AE03-B366343DE558">_OPERATION_START_PARAMETERS</a> structure that specifies <b>VERSION</b>, <b>OPERATION_ID</b> and <b>FLAGS</b>.


## -returns



<b>TRUE</b> for all valid parameters and <b>FALSE</b> otherwise.  To get extended error information, call <b>GetLastError</b>. 




## -remarks



The version of the <a href="https://msdn.microsoft.com/51AE0017-2CDE-4BCD-AE03-B366343DE558">_OPERATION_START_PARAMETERS</a> structure is defined as <b>OPERATION_API_VERSION</b> in the Windows SDK. 

Because the <b>OperationStart</b> function is synchronous, it can take several seconds to return. This should be avoided in UI threads for the best responsiveness.

There is a single instance of the operation recorder in a process. Although the operation  recorder APIs can be called from multiple threads within the process, all calls act on the single instance.

Application launch tracing lasts for the first 10 second of the process lifetime.  <b>OperationStart</b> should be called after the end of application launch tracing by the system. 

Every call to <b>OperationStart</b> must be followed by a call to <a href="https://msdn.microsoft.com/73C6FBDD-BB4A-46A5-8E39-7862A1938F47">OperationEnd</a>. Otherwise, the operation trace will be discarded after about 10s.

The maximum number of operations that can be recorded on a given system is configurable. If this maximum is exceeded, the least recently used prefetch files are replaced. 

On Windows 8, this functionality requires the Superfetch service to be enabled. Windows 8 will have the service enabled by default. 
For Windows Server 2012, this prefetching functionality needs to be enabled and disabled as required. This can be done using CIM based PowerShell cmdlets.  The prefetcher functionality can be exposed using the <a href="https://msdn.microsoft.com/2335d397-234f-4122-8c3e-44986d6ed0ca">CIM class</a>  of the <b>CIM_PrefetcherService</b>.



#### Examples

<pre class="syntax" xml:space="preserve"><code>    BOOL Success;
    DWORD ErrorCode;
    OPERATION_START_PARAMETERS OpStart;
    OPERATION_END_PARAMETERS OpEnd;

    // We want to notify Windows that we are going to be performing some          
    // disk-bound work that repeatedly access the same file data. The system will 
    // try to record data about our activity to make future operations faster.    
    
    ZeroMemory(&amp;OpStart, sizeof(OpStart));
    OpStart.Version = OPERATION_API_VERSION;
    OpStart.OperationId = MY_OPERATION_ID_1;

    ZeroMemory(&amp;OpEnd, sizeof(OpEnd));
    OpEnd.Version = OPERATION_API_VERSION;
    OpEnd.OperationId = MY_OPERATION_ID_1;
 
    // We want the system to only record activity in this thread.

    OpStart.Flags = OPERATION_START_TRACE_CURRENT_THREAD;
    OpEnd.Flags = 0;

    Success = OperationStart(&amp;OpStart);

    if (!Success) {
        ErrorCode = GetLastError();
        fprintf(stderr, "OperationStart failed: %d\n", ErrorCode);

        // We could not notify the system about our operation. That's OK.
  
                  }

    // Perform the disk-bound work that should be recorded here.  
    // This may involve opening/reading many files or loading     
    // and running many DLLs.                                    

    Success = OperationEnd(&amp;OpEnd);

    if (!Success) {
        fprintf(stderr, "OperationEnd failed: %d\n", GetLastError());
                  }

</code></pre>



## -see-also




<b></b>



<a href="https://msdn.microsoft.com/D5446D23-DBB5-4EB8-97E4-590537A33193">OPERATION_ID</a>



<a href="https://msdn.microsoft.com/c1051b62-0e67-4480-81c6-cb138d3296d6">Operation Recorder</a>



<a href="https://msdn.microsoft.com/73C6FBDD-BB4A-46A5-8E39-7862A1938F47">OperationEnd</a>



<a href="https://msdn.microsoft.com/45ABFE6A-7B70-418F-8C3C-6388079D1306">_OPERATION_END_PARAMETERS</a>



<a href="https://msdn.microsoft.com/51AE0017-2CDE-4BCD-AE03-B366343DE558">_OPERATION_START_PARAMETERS</a>
 

 

