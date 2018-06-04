---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# MsiDatabaseExportW function


## -description


The 
<b>MsiDatabaseExport</b> function exports a Microsoft Installer table from an open database to a <a href="https://msdn.microsoft.com/49210242-bd32-4e5c-b782-a132d670fdfe">Text Archive File</a>.


## -parameters




### -param hDatabase [in]

The handle to a database  from <a href="https://msdn.microsoft.com/984996e3-aa2c-49ff-9067-ebefd3afdecb">MsiOpenDatabase</a>.


### -param szTableName [in]

The name of the table to export.


### -param szFolderPath [in]

The name of the folder that contains archive files.


### -param szFileName [in]

The name of the exported table archive file.


## -returns




					The 
<b>MsiDatabaseExport</b> function returns one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_PATHNAME</b></dt>
</dl>
</td>
<td width="60%">
An invalid path is passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The function fails.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
An invalid or inactive handle is supplied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter is passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function succeeds.

</td>
</tr>
</table>
 




## -remarks



If a table contains streams, 
<b>MsiDatabaseExport</b> exports each stream to a separate file.

For more information, see 
<a href="https://msdn.microsoft.com/df277641-393e-4202-bb92-4b813ddaa0ca">MsiDatabaseImport</a>.

This function cannot be called from custom actions. A call to this function from a custom action causes the function to fail.

If the function fails, you can get extended error information by using <a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>.




## -see-also




<a href="database_functions.htm">Database Management Functions</a>



<a href="https://msdn.microsoft.com/49210242-bd32-4e5c-b782-a132d670fdfe">Text Archive Files</a>
 

 

