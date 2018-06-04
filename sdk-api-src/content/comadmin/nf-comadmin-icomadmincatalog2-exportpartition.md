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

# ICOMAdminCatalog2::ExportPartition


## -description


Exports a partition to a file.

An exported partition can be imported using the <a href="https://msdn.microsoft.com/e1f54a6a-9b90-4e9e-b94c-46f6c9b683a3">InstallPartition</a> method.


## -parameters




### -param bstrPartitionIDOrName [in]

The partition GUID or name of the partition.


### -param bstrPartitionFileName [in]

The file to which the specified partition is exported. If no path is specified, the current directory is used. If no file name is specified, the application name is used.


### -param lOptions [in]

The option flags. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="COMAdminExportNoUsers"></a><a id="comadminexportnousers"></a><a id="COMADMINEXPORTNOUSERS"></a><dl>
<dt><b>COMAdminExportNoUsers</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Do not export users with roles (default).

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdminExportUsers"></a><a id="comadminexportusers"></a><a id="COMADMINEXPORTUSERS"></a><dl>
<dt><b>COMAdminExportUsers</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Export users with roles.

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdminExportApplicationProxy"></a><a id="comadminexportapplicationproxy"></a><a id="COMADMINEXPORTAPPLICATIONPROXY"></a><dl>
<dt><b>COMAdminExportApplicationProxy</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Export applications as proxies.


</td>
</tr>
<tr>
<td width="40%"><a id="COMAdminExportForceOverwriteOfFile"></a><a id="comadminexportforceoverwriteoffile"></a><a id="COMADMINEXPORTFORCEOVERWRITEOFFILE"></a><dl>
<dt><b>COMAdminExportForceOverwriteOfFile</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Overwrite existing files.

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdminExportIn10Format"></a><a id="comadminexportin10format"></a><a id="COMADMINEXPORTIN10FORMAT"></a><dl>
<dt><b>COMAdminExportIn10Format</b></dt>
<dt>16</dt>
</dl>
</td>
<td width="60%">
Export in COM+ 1.0 format.


</td>
</tr>
</table>
 


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COMADMIN_E_OBJECT_DOES_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The specified partition does not exist.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ffca611d-dacc-47be-9101-9de76ecc8393">ICOMAdminCatalog2</a>
 

 

