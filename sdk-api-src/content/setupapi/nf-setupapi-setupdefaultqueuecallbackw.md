---
UID: NF:setupapi.SetupDefaultQueueCallbackW
title: SetupDefaultQueueCallbackW function (setupapi.h)
author: windows-sdk-content
description: The SetupDefaultQueueCallback function is the default queue callback routine included with the Setup API. You can use it to process notifications sent by the SetupCommitFileQueue function.
old-location: setup\setupdefaultqueuecallback.htm
tech.root: SetupApi
ms.assetid: e03f43b9-fe34-4340-86f3-c353df6c6db0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SPFILENOTIFY_COPYERROR, SPFILENOTIFY_DELETEERROR, SPFILENOTIFY_ENDCOPY, SPFILENOTIFY_ENDDELETE, SPFILENOTIFY_ENDQUEUE, SPFILENOTIFY_ENDRENAME, SPFILENOTIFY_ENDSUBQUEUE, SPFILENOTIFY_LANGMISMATCH, SPFILENOTIFY_NEEDMEDIA, SPFILENOTIFY_RENAMEERROR, SPFILENOTIFY_STARTCOPY, SPFILENOTIFY_STARTDELETE, SPFILENOTIFY_STARTQUEUE, SPFILENOTIFY_STARTRENAME, SPFILENOTIFY_STARTSUBQUEUE, SPFILENOTIFY_TARGETEXISTS, SPFILENOTIFY_TARGETNEWER, SetupDefaultQueueCallback, SetupDefaultQueueCallback function [Setup API], SetupDefaultQueueCallbackA, SetupDefaultQueueCallbackW, _setupapi_setupdefaultqueuecallback, setup.setupdefaultqueuecallback, setupapi/SetupDefaultQueueCallback, setupapi/SetupDefaultQueueCallbackA, setupapi/SetupDefaultQueueCallbackW
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupDefaultQueueCallbackW (Unicode) and SetupDefaultQueueCallbackA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
 - SetupDefaultQueueCallback
 - SetupDefaultQueueCallbackA
 - SetupDefaultQueueCallbackW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDefaultQueueCallbackW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupDefaultQueueCallback</b> function is the default queue callback routine included with the Setup API. You can use it to process notifications sent by the 
<a href="https://msdn.microsoft.com/c532f435-7393-49f0-975c-4c0ecca64407">SetupCommitFileQueue</a> function.


## -parameters




### -param Context [in]

Pointer to the context initialized by the 
<a href="https://msdn.microsoft.com/3ee7da67-42ff-4ea1-9c7f-6c0dcc3dc0b4">SetupInitDefaultQueueCallback</a> or 
<a href="https://msdn.microsoft.com/9376f55b-55ee-4064-8aed-264c43db0c7d">SetupInitDefaultQueueCallbackEx</a> functions.


### -param Notification [in]

Notification of a queue action. This parameter can be one of the  values shown in the following table. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPFILENOTIFY_STARTQUEUE"></a><a id="spfilenotify_startqueue"></a><dl>
<dt><b>SPFILENOTIFY_STARTQUEUE</b></dt>
</dl>
</td>
<td width="60%">
Started queued file operations.

</td>
</tr>
<tr>
<td width="40%"><a id="SPFILENOTIFY_ENDQUEUE"></a><a id="spfilenotify_endqueue"></a><dl>
<dt><b>SPFILENOTIFY_ENDQUEUE</b></dt>
</dl>
</td>
<td width="60%">
Finished queued file operations.

</td>
</tr>
<tr>
<td width="40%"><a id="SPFILENOTIFY_STARTSUBQUEUE"></a><a id="spfilenotify_startsubqueue"></a><dl>
<dt><b>SPFILENOTIFY_STARTSUBQUEUE</b></dt>
</dl>
</td>
<td width="60%">
Started a copy, rename, or delete subqueue.

</td>
</tr>
<tr>
<td width="40%"><a id="SPFILENOTIFY_ENDSUBQUEUE"></a><a id="spfilenotify_endsubqueue"></a><dl>
<dt><b>SPFILENOTIFY_ENDSUBQUEUE</b></dt>
</dl>
</td>
<td width="60%">
Finished a copy, rename, or delete subqueue.

</td>
</tr>
<tr>
<td width="40%"><a id="SPFILENOTIFY_STARTRENAME"></a><a id="spfilenotify_startrename"></a><dl>
<dt><b>SPFILENOTIFY_STARTRENAME</b></dt>
</dl>
</td>
<td width="60%">
Started a rename operation.

</td>
</tr>
<tr>
<td width="40%"><a id="SPFILENOTIFY_ENDRENAME"></a><a id="spfilenotify_endrename"></a><dl>
<dt><b>SPFILENOTIFY_ENDRENAME</b></dt>
</dl>
</td>
<td width="60%">
Finished a rename operation.

</td>
</tr>
<tr>
<td width="40%"><a id="SPFILENOTIFY_RENAMEERROR"></a><a id="spfilenotify_renameerror"></a><dl>
<dt><b>SPFILENOTIFY_RENAMEERROR</b></dt>
</dl>
</td>
<td width="60%">
Encountered an error while renaming a file.

</td>
</tr>
<tr>
<td width="40%"><a id="SPFILENOTIFY_STARTDELETE"></a><a id="spfilenotify_startdelete"></a><dl>
<dt><b>SPFILENOTIFY_STARTDELETE</b></dt>
</dl>
</td>
<td width="60%">
Started a delete operation.

</td>
</tr>
<tr>
<td width="40%"><a id="SPFILENOTIFY_ENDDELETE"></a><a id="spfilenotify_enddelete"></a><dl>
<dt><b>SPFILENOTIFY_ENDDELETE</b></dt>
</dl>
</td>
<td width="60%">
Finished a delete operation.

</td>
</tr>
<tr>
<td width="40%"><a id="SPFILENOTIFY_DELETEERROR"></a><a id="spfilenotify_deleteerror"></a><dl>
<dt><b>SPFILENOTIFY_DELETEERROR</b></dt>
</dl>
</td>
<td width="60%">
Encountered an error while deleting a file.

</td>
</tr>
<tr>
<td width="40%"><a id="SPFILENOTIFY_STARTCOPY"></a><a id="spfilenotify_startcopy"></a><dl>
<dt><b>SPFILENOTIFY_STARTCOPY</b></dt>
</dl>
</td>
<td width="60%">
Started a copy operation.

</td>
</tr>
<tr>
<td width="40%"><a id="SPFILENOTIFY_ENDCOPY"></a><a id="spfilenotify_endcopy"></a><dl>
<dt><b>SPFILENOTIFY_ENDCOPY</b></dt>
</dl>
</td>
<td width="60%">
Finished a copy operation.

</td>
</tr>
<tr>
<td width="40%"><a id="SPFILENOTIFY_COPYERROR"></a><a id="spfilenotify_copyerror"></a><dl>
<dt><b>SPFILENOTIFY_COPYERROR</b></dt>
</dl>
</td>
<td width="60%">
Encountered an error while copying a file.

</td>
</tr>
<tr>
<td width="40%"><a id="SPFILENOTIFY_NEEDMEDIA"></a><a id="spfilenotify_needmedia"></a><dl>
<dt><b>SPFILENOTIFY_NEEDMEDIA</b></dt>
</dl>
</td>
<td width="60%">
New media is required.

</td>
</tr>
<tr>
<td width="40%"><a id="SPFILENOTIFY_LANGMISMATCH"></a><a id="spfilenotify_langmismatch"></a><dl>
<dt><b>SPFILENOTIFY_LANGMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
Existing target file is in a different language than the source.

</td>
</tr>
<tr>
<td width="40%"><a id="SPFILENOTIFY_TARGETEXISTS"></a><a id="spfilenotify_targetexists"></a><dl>
<dt><b>SPFILENOTIFY_TARGETEXISTS</b></dt>
</dl>
</td>
<td width="60%">
Target file exists.

</td>
</tr>
<tr>
<td width="40%"><a id="SPFILENOTIFY_TARGETNEWER_"></a><a id="spfilenotify_targetnewer_"></a><dl>
<dt><b>SPFILENOTIFY_TARGETNEWER </b></dt>
</dl>
</td>
<td width="60%">
Existing target file is newer than source.

</td>
</tr>
</table>
 


### -param Param1 [in]

Additional message information. The content of this parameter depends on the value of the <i>Notification</i> parameter.


### -param Param2 [in]

Additional message information. The content of this parameter depends on the value of the <i>Notification</i> parameter.


## -returns



Returns an unsigned integer to 
<a href="https://msdn.microsoft.com/c532f435-7393-49f0-975c-4c0ecca64407">SetupCommitFileQueue</a> that can be the one of the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILEOP_ABORT</b></dt>
</dl>
</td>
<td width="60%">
Aborts the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILEOP_DOIT</b></dt>
</dl>
</td>
<td width="60%">
Performs the file operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILEOP_SKIP</b></dt>
</dl>
</td>
<td width="60%">
Skips the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILEOP_RETRY</b></dt>
</dl>
</td>
<td width="60%">
Retries the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILEOP_NEWPATH</b></dt>
</dl>
</td>
<td width="60%">
Gets a new path for the operation.

</td>
</tr>
</table>
 

To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>SetupDefaultQueueCallback</b> function is usually only called explicitly by a custom queue callback routine. The custom callback handles a subset of the queue commit notifications and calls the 
<b>SetupDefaultQueueCallback</b> function to handle the rest of the notifications.

For more information see, 
<a href="https://msdn.microsoft.com/866e1066-b6e0-43d3-8af4-bd37fbc024e2">Queue Notifications</a>.




## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/c532f435-7393-49f0-975c-4c0ecca64407">SetupCommitFileQueue</a>
 

 

