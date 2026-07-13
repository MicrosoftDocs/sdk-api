---
UID: NF:setupapi.SetupCommitFileQueueA
title: SetupCommitFileQueueA function (setupapi.h)
description: The SetupCommitFileQueue function performs file operations queued on a setup file queue. (ANSI)
helpviewer_keywords: ["SetupCommitFileQueueA", "setupapi/SetupCommitFileQueueA"]
old-location: setup\setupcommitfilequeue.htm
tech.root: setup
ms.assetid: c532f435-7393-49f0-975c-4c0ecca64407
ms.date: 12/05/2018
ms.keywords: SetupCommitFileQueue, SetupCommitFileQueue function [Setup API], SetupCommitFileQueueA, SetupCommitFileQueueW, _setupapi_setupcommitfilequeue, setup.setupcommitfilequeue, setupapi/SetupCommitFileQueue, setupapi/SetupCommitFileQueueA, setupapi/SetupCommitFileQueueW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupCommitFileQueueW (Unicode) and SetupCommitFileQueueA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupCommitFileQueueA
 - setupapi/SetupCommitFileQueueA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupCommitFileQueue
 - SetupCommitFileQueueA
 - SetupCommitFileQueueW
---

# SetupCommitFileQueueA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupCommitFileQueue</b> function performs file operations queued on a setup file queue.

The best practice is to collect all the required file operations for the file queue and commit the queue only once because a file queue cannot be reused after it has been committed. If additional processing of the queue is required after it has been committed, the handle to the queue should be closed and a new file queue created. For more information, see 
<a href="/windows/desktop/SetupApi/committing-a-queue">Committing a Queue</a>.

If a file is modified, the caller of this function is required have privileges to write into the target directory.

## -parameters

### -param Owner [in]

Optional handle to a window to use as the parent of any progress dialog boxes.

### -param QueueHandle [in]

Handle to a setup file queue, as returned by 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupopenfilequeue">SetupOpenFileQueue</a>.

### -param MsgHandler [in]

Pointer to an optional callback routine to be notified of various significant events that are in the queue processing. For more information, see 
<a href="/windows/desktop/SetupApi/default-queue-callback-routine">Default Queue Callback Routine</a> or 
<a href="/windows/desktop/api/setupapi/nc-setupapi-psp_file_callback_a">FileCallback</a> If the callback routine is <b>null</b>, 
<b>SetupCommitFileQueue</b> returns <b>TRUE</b> and the error is 0 or NO_ERROR.

### -param Context [in]

Value that is passed to the callback function supplied by the <i>MsgHandler</i> parameter. If the default callback routine has been specified as <i>MsgHandler</i>, this context must be the context returned from 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinitdefaultqueuecallback">SetupInitDefaultQueueCallback</a> or 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupinitdefaultqueuecallbackex">SetupInitDefaultQueueCallbackEx</a>.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The callback routine specified in <i>MsgHandler</i> should be compatible with the parameters that 
<b>SetupCommitFileQueue</b> passed to it during a queue commit.

If Unicode is defined in your callback application, and you specify <i>MsgHandler</i> as the default queue callback routine, the callback routine will expect Unicode parameters. Otherwise, the default queue callback routine will expect ANSI parameters.





> [!NOTE]
> The setupapi.h header defines SetupCommitFileQueue as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupclosefilequeue">SetupCloseFileQueue</a>
