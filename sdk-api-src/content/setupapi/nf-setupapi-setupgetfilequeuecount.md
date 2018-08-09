---
UID: NF:setupapi.SetupGetFileQueueCount
title: SetupGetFileQueueCount function
author: windows-sdk-content
description: The SetupGetFileQueueCount function gets the count from a setup file queue.
old-location: setup\setupgetfilequeuecount.htm
old-project: SetupApi
ms.assetid: 57312fa3-8ffc-47be-b344-3780d13ed175
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FILEOP_BACKUP, FILEOP_COPY, FILEOP_DELETE, FILEOP_RENAME, SetupGetFileQueueCount, SetupGetFileQueueCount function [Setup API], _setupapi_setupgetfilequeuecount, setup.setupgetfilequeuecount, setupapi/SetupGetFileQueueCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupGetFileQueueCount
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupGetFileQueueCount function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetFileQueueCount</b> function gets the count from a setup file queue.


## -parameters




### -param FileQueue [in]

Handle to an open setup file queue.


### -param SubQueueFileOp [in]

Flag that specifies which subqueue count to be returned. 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILEOP_COPY"></a><a id="fileop_copy"></a><dl>
<dt><b>FILEOP_COPY</b></dt>
</dl>
</td>
<td width="60%">
Return the number of entries in the copy subqueue.

</td>
</tr>
<tr>
<td width="40%"><a id="FILEOP_RENAME"></a><a id="fileop_rename"></a><dl>
<dt><b>FILEOP_RENAME</b></dt>
</dl>
</td>
<td width="60%">
Return the number of entries in the rename subqueue.

</td>
</tr>
<tr>
<td width="40%"><a id="FILEOP_DELETE"></a><a id="fileop_delete"></a><dl>
<dt><b>FILEOP_DELETE</b></dt>
</dl>
</td>
<td width="60%">
Return the number of entries in the delete subqueue.

</td>
</tr>
<tr>
<td width="40%"><a id="FILEOP_BACKUP"></a><a id="fileop_backup"></a><dl>
<dt><b>FILEOP_BACKUP</b></dt>
</dl>
</td>
<td width="60%">
Return the number of entries in the backup subqueue.

</td>
</tr>
</table>
 


### -param NumOperations [out]

Count from the setup file queue.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is 0 (zero). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>
 

 

