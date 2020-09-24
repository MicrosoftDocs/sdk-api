---
UID: NF:comadmin.ICOMAdminCatalog.ExportApplication
title: ICOMAdminCatalog::ExportApplication (comadmin.h)
description: Exports a COM+ application or application proxy to a file, ready for installation on different computers.
helpviewer_keywords: ["COMAdminExportApplicationProxy","COMAdminExportForceOverwriteOfFile","COMAdminExportIn10Format","COMAdminExportNoUsers","COMAdminExportUsers","ExportApplication","ExportApplication method [COM+]","ExportApplication method [COM+]","ICOMAdminCatalog interface","ICOMAdminCatalog interface [COM+]","ExportApplication method","ICOMAdminCatalog.ExportApplication","ICOMAdminCatalog::ExportApplication","_cos_ICOMAdminCatalog_ExportApplication","comadmin/ICOMAdminCatalog::ExportApplication","cos.icomadmincatalog_exportapplication"]
old-location: cos\icomadmincatalog_exportapplication.htm
tech.root: cos
ms.assetid: 431c0299-56c2-4ec3-8ecc-ee1cbec3eff6
ms.date: 12/05/2018
ms.keywords: COMAdminExportApplicationProxy, COMAdminExportForceOverwriteOfFile, COMAdminExportIn10Format, COMAdminExportNoUsers, COMAdminExportUsers, ExportApplication, ExportApplication method [COM+], ExportApplication method [COM+],ICOMAdminCatalog interface, ICOMAdminCatalog interface [COM+],ExportApplication method, ICOMAdminCatalog.ExportApplication, ICOMAdminCatalog::ExportApplication, _cos_ICOMAdminCatalog_ExportApplication, comadmin/ICOMAdminCatalog::ExportApplication, cos.icomadmincatalog_exportapplication
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ICOMAdminCatalog::ExportApplication
 - comadmin/ICOMAdminCatalog::ExportApplication
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
 - ICOMAdminCatalog.ExportApplication
---

# ICOMAdminCatalog::ExportApplication


## -description

Exports a COM+ application or application proxy to a file, ready for installation on different computers.

## -parameters

### -param bstrApplIDOrName [in]

The GUID or application name of the application to be exported.

### -param bstrApplicationFile [in]

The name of the file to export the application to, including the file path. If this parameter is <b>NULL</b> or an empty string, the <b>ExportApplication</b> method returns E_INVALIDARG.
If the path is not specified, the current directory is used.
If a relative path is entered, the path is relative to the current directory.

### -param lOptions [in]

Specifies the application export options. This parameter can be one of more of the following values from the <b>COMAdminApplicationExportOptions</b> enumeration type.

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
Export without the users assigned to application roles.

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdminExportUsers"></a><a id="comadminexportusers"></a><a id="COMADMINEXPORTUSERS"></a><dl>
<dt><b>COMAdminExportUsers</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Export with the users assigned to application roles.

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
Export in COM+ 1.0 (Windows 2000) format.

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
The application does not exist.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog">ICOMAdminCatalog</a>