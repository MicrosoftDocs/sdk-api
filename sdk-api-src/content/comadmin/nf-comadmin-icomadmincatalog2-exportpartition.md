---
UID: NF:comadmin.ICOMAdminCatalog2.ExportPartition
title: ICOMAdminCatalog2::ExportPartition
author: windows-sdk-content
description: Exports a partition to a file.
old-location: cos\icomadmincatalog2_exportpartition.htm
old-project: cossdk
ms.assetid: cc793025-e8d9-4dcb-a55d-81dec38d05b9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: COMAdminExportApplicationProxy, COMAdminExportForceOverwriteOfFile, COMAdminExportIn10Format, COMAdminExportNoUsers, COMAdminExportUsers, ExportPartition, ExportPartition method [COM+], ExportPartition method [COM+],ICOMAdminCatalog2 interface, ICOMAdminCatalog2 interface [COM+],ExportPartition method, ICOMAdminCatalog2.ExportPartition, ICOMAdminCatalog2::ExportPartition, _cos_icomadmincatalog2_ExportPartition, comadmin/ICOMAdminCatalog2::ExportPartition, cos.icomadmincatalog2_exportpartition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comadmin.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: COMAdminTxIsolationLevelOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog2.ExportPartition
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICOMAdminCatalog2::ExportPartition


## -description


Exports a partition to a file.

An exported partition can be imported using the <a href="https://msdn.microsoft.com/en-us/library/ms687112(v=VS.85).aspx">InstallPartition</a> method.


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




<a href="https://msdn.microsoft.com/en-us/library/Ee309562(v=VS.85).aspx">ICOMAdminCatalog2</a>
 

 

