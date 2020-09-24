---
UID: NF:comadmin.ICOMAdminCatalog2.ExportPartition
title: ICOMAdminCatalog2::ExportPartition (comadmin.h)
description: Exports a partition to a file.
helpviewer_keywords: ["COMAdminExportApplicationProxy","COMAdminExportForceOverwriteOfFile","COMAdminExportIn10Format","COMAdminExportNoUsers","COMAdminExportUsers","ExportPartition","ExportPartition method [COM+]","ExportPartition method [COM+]","ICOMAdminCatalog2 interface","ICOMAdminCatalog2 interface [COM+]","ExportPartition method","ICOMAdminCatalog2.ExportPartition","ICOMAdminCatalog2::ExportPartition","_cos_icomadmincatalog2_ExportPartition","comadmin/ICOMAdminCatalog2::ExportPartition","cos.icomadmincatalog2_exportpartition"]
old-location: cos\icomadmincatalog2_exportpartition.htm
tech.root: cos
ms.assetid: cc793025-e8d9-4dcb-a55d-81dec38d05b9
ms.date: 12/05/2018
ms.keywords: COMAdminExportApplicationProxy, COMAdminExportForceOverwriteOfFile, COMAdminExportIn10Format, COMAdminExportNoUsers, COMAdminExportUsers, ExportPartition, ExportPartition method [COM+], ExportPartition method [COM+],ICOMAdminCatalog2 interface, ICOMAdminCatalog2 interface [COM+],ExportPartition method, ICOMAdminCatalog2.ExportPartition, ICOMAdminCatalog2::ExportPartition, _cos_icomadmincatalog2_ExportPartition, comadmin/ICOMAdminCatalog2::ExportPartition, cos.icomadmincatalog2_exportpartition
req.header: comadmin.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICOMAdminCatalog2::ExportPartition
 - comadmin/ICOMAdminCatalog2::ExportPartition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog2.ExportPartition
---

# ICOMAdminCatalog2::ExportPartition


## -description

Exports a partition to a file.

An exported partition can be imported using the <a href="/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-installpartition">InstallPartition</a> method.

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

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog2">ICOMAdminCatalog2</a>