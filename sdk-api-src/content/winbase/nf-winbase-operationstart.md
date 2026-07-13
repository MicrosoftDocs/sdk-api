---
UID: NF:winbase.OperationStart
title: OperationStart function (winbase.h)
description: Notifies the system that the application is about to start an operation.
helpviewer_keywords: ["OperationStart","OperationStart function [Operation Recorder]","oprec.operationstart","winbase/OperationStart"]
old-location: oprec\operationstart.htm
tech.root: oprec
ms.assetid: 3E67057E-D09F-48BA-A95A-5D00F4783D9C
ms.date: 12/05/2018
ms.keywords: OperationStart, OperationStart function [Operation Recorder], oprec.operationstart, winbase/OperationStart
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OperationStart
 - winbase/OperationStart
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - OperationStart
---

# OperationStart function


## -description

Notifies the system that the application is about to start an operation.

 If an application calls <b>OperationStart</b> with a valid <a href="/previous-versions/windows/desktop/oprec/operation-id">OPERATION_ID</a> value, the system records the specified operation’s file access patterns until <a href="/windows/desktop/api/winbase/nf-winbase-operationend">OperationEnd</a> is called for the same operation ID. This record is stored in a <i>filename.pf</i> prefetch file. Every call to <b>OperationStart</b> must be followed by a call to <b>OperationEnd</b>, otherwise the operation's record is discarded after 10 seconds.


If an application calls <b>OperationStart</b> for an operation ID for which a prefetch file exists, the system loads the operation's files into memory prior to running the operation. The recording process remains the same and the system updates the appropriate <i>filename.pf</i> prefetch file.

## -parameters

### -param OperationStartParams [in]

An <a href="/windows/desktop/api/winbase/ns-winbase-operation_start_parameters">_OPERATION_START_PARAMETERS</a> structure that specifies <b>VERSION</b>, <b>OPERATION_ID</b> and <b>FLAGS</b>.

## -returns

<b>TRUE</b> for all valid parameters and <b>FALSE</b> otherwise.  To get extended error information, call <b>GetLastError</b>.

## -remarks

The version of the <a href="/windows/desktop/api/winbase/ns-winbase-operation_start_parameters">_OPERATION_START_PARAMETERS</a> structure is defined as <b>OPERATION_API_VERSION</b> in the Windows SDK. 

Because the <b>OperationStart</b> function is synchronous, it can take several seconds to return. This should be avoided in UI threads for the best responsiveness.

There is a single instance of the operation recorder in a process. Although the operation  recorder APIs can be called from multiple threads within the process, all calls act on the single instance.

Application launch tracing lasts for the first 10 second of the process lifetime.  <b>OperationStart</b> should be called after the end of application launch tracing by the system. 

Every call to <b>OperationStart</b> must be followed by a call to <a href="/windows/desktop/api/winbase/nf-winbase-operationend">OperationEnd</a>. Otherwise, the operation trace will be discarded after about 10s.

The maximum number of operations that can be recorded on a given system is configurable. If this maximum is exceeded, the least recently used prefetch files are replaced. 

On Windows 8, this functionality requires the Superfetch service to be enabled. Windows 8 will have the service enabled by default. 
For Windows Server 2012, this prefetching functionality needs to be enabled and disabled as required. This can be done using CIM based PowerShell cmdlets.  The prefetcher functionality can be exposed using the <a href="/windows/desktop/WmiSdk/cimclas">CIM class</a>  of the <b>CIM_PrefetcherService</b>.



#### Examples


``` syntax
    BOOL Success;
    DWORD ErrorCode;
    OPERATION_START_PARAMETERS OpStart;
    OPERATION_END_PARAMETERS OpEnd;

    // We want to notify Windows that we are going to be performing some          
    // disk-bound work that repeatedly access the same file data. The system will 
    // try to record data about our activity to make future operations faster.    
    
    ZeroMemory(&OpStart, sizeof(OpStart));
    OpStart.Version = OPERATION_API_VERSION;
    OpStart.OperationId = MY_OPERATION_ID_1;

    ZeroMemory(&OpEnd, sizeof(OpEnd));
    OpEnd.Version = OPERATION_API_VERSION;
    OpEnd.OperationId = MY_OPERATION_ID_1;
 
    // We want the system to only record activity in this thread.

    OpStart.Flags = OPERATION_START_TRACE_CURRENT_THREAD;
    OpEnd.Flags = 0;

    Success = OperationStart(&OpStart);

    if (!Success) {
        ErrorCode = GetLastError();
        fprintf(stderr, "OperationStart failed: %d\n", ErrorCode);

        // We could not notify the system about our operation. That's OK.
  
                  }

    // Perform the disk-bound work that should be recorded here.  
    // This may involve opening/reading many files or loading     
    // and running many DLLs.                                    

    Success = OperationEnd(&OpEnd);

    if (!Success) {
        fprintf(stderr, "OperationEnd failed: %d\n", GetLastError());
                  }


```


## -see-also

<b></b>



<a href="/previous-versions/windows/desktop/oprec/operation-id">OPERATION_ID</a>



<a href="/previous-versions/windows/desktop/oprec/-operation-portal">Operation Recorder</a>



<a href="/windows/desktop/api/winbase/nf-winbase-operationend">OperationEnd</a>



<a href="/windows/desktop/api/winbase/ns-winbase-operation_end_parameters">_OPERATION_END_PARAMETERS</a>



<a href="/windows/desktop/api/winbase/ns-winbase-operation_start_parameters">_OPERATION_START_PARAMETERS</a>
