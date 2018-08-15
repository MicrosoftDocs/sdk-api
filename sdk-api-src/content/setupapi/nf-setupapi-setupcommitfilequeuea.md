---
UID: NF:setupapi.SetupCommitFileQueueA
title: SetupCommitFileQueueA function
author: windows-sdk-content
description: The SetupCommitFileQueue function performs file operations queued on a setup file queue.
old-location: setup\setupcommitfilequeue.htm
old-project: SetupApi
ms.assetid: c532f435-7393-49f0-975c-4c0ecca64407
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: SetupCommitFileQueue, SetupCommitFileQueue function [Setup API], SetupCommitFileQueueA, SetupCommitFileQueueW, _setupapi_setupcommitfilequeue, setup.setupcommitfilequeue, setupapi/SetupCommitFileQueue, setupapi/SetupCommitFileQueueA, setupapi/SetupCommitFileQueueW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
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
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupCommitFileQueueA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupCommitFileQueue</b> function performs file operations queued on a setup file queue.

The best practice is to collect all the required file operations for the file queue and commit the queue only once because a file queue cannot be reused after it has been committed. If additional processing of the queue is required after it has been committed, the handle to the queue should be closed and a new file queue created. For more information, see 
<a href="https://msdn.microsoft.com/536f47f5-785e-4a83-a500-c769442e3e68">Committing a Queue</a>.

If a file is modified, the caller of this function is required have privileges to write into the target directory.


## -parameters




### -param Owner [in]

Optional handle to a window to use as the parent of any progress dialog boxes.


### -param QueueHandle [in]

Handle to a setup file queue, as returned by 
<a href="https://msdn.microsoft.com/36950f18-80ae-46b7-9f9f-bd5307d72a3b">SetupOpenFileQueue</a>.


### -param MsgHandler [in]

Pointer to an optional callback routine to be notified of various significant events that are in the queue processing. For more information, see 
<a href="https://msdn.microsoft.com/c6ba6398-4119-4bdd-b264-1bc645800b03">Default Queue Callback Routine</a> or 
<a href="https://msdn.microsoft.com/41eaa57a-e116-443c-93ee-397456a5c466">FileCallback</a> If the callback routine is <b>null</b>, 
<b>SetupCommitFileQueue</b> returns <b>TRUE</b> and the error is 0 or NO_ERROR.


### -param Context [in]

Value that is passed to the callback function supplied by the <i>MsgHandler</i> parameter. If the default callback routine has been specified as <i>MsgHandler</i>, this context must be the context returned from 
<a href="https://msdn.microsoft.com/3ee7da67-42ff-4ea1-9c7f-6c0dcc3dc0b4">SetupInitDefaultQueueCallback</a> or 
<a href="https://msdn.microsoft.com/9376f55b-55ee-4064-8aed-264c43db0c7d">SetupInitDefaultQueueCallbackEx</a>.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The callback routine specified in <i>MsgHandler</i> should be compatible with the parameters that 
<b>SetupCommitFileQueue</b> passed to it during a queue commit.

If Unicode is defined in your callback application, and you specify <i>MsgHandler</i> as the default queue callback routine, the callback routine will expect Unicode parameters. Otherwise, the default queue callback routine will expect ANSI parameters.




## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/51c63e65-a844-46b4-93ef-8a92a9c8a604">SetupCloseFileQueue</a>
 

 

