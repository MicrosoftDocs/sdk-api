---
UID: NF:setupapi.SetupGetFileQueueCount
title: SetupGetFileQueueCount function (setupapi.h)
description: The SetupGetFileQueueCount function gets the count from a setup file queue.
helpviewer_keywords: ["FILEOP_BACKUP","FILEOP_COPY","FILEOP_DELETE","FILEOP_RENAME","SetupGetFileQueueCount","SetupGetFileQueueCount function [Setup API]","_setupapi_setupgetfilequeuecount","setup.setupgetfilequeuecount","setupapi/SetupGetFileQueueCount"]
old-location: setup\setupgetfilequeuecount.htm
tech.root: setup
ms.assetid: 57312fa3-8ffc-47be-b344-3780d13ed175
ms.date: 12/05/2018
ms.keywords: FILEOP_BACKUP, FILEOP_COPY, FILEOP_DELETE, FILEOP_RENAME, SetupGetFileQueueCount, SetupGetFileQueueCount function [Setup API], _setupapi_setupgetfilequeuecount, setup.setupgetfilequeuecount, setupapi/SetupGetFileQueueCount
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
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupGetFileQueueCount
 - setupapi/SetupGetFileQueueCount
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
 - SetupGetFileQueueCount
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
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>