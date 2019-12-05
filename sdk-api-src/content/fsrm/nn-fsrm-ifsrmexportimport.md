---
UID: NN:fsrm.IFsrmExportImport
title: IFsrmExportImport (fsrm.h)
description: Used to export and import FSRM objects.
old-location: fsrm\ifsrmexportimport.htm
tech.root: fsrm
ms.assetid: 5a3b682e-d2c3-43b3-9d10-4bba9d9c81d4
ms.date: 12/05/2018
ms.keywords: IFsrmExportImport, IFsrmExportImport interface [File Server Resource Manager], IFsrmExportImport interface [File Server Resource Manager],described, fs.ifsrmexportimport, fsrm.ifsrmexportimport, fsrm/IFsrmExportImport
ms.topic: interface
f1_keywords:
- fsrm/IFsrmExportImport
dev_langs:
- c++
req.header: fsrm.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- SrmSvc.dll
api_name:
- IFsrmExportImport
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmExportImport interface


## -description


Used to export and import FSRM objects.
<div class="alert"><b>Note</b>  This interface supports local use only. Remote operations are not supported.</div><div> </div>To get this interface, call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmExportImport</b> as the class identifier and 
    <code>__uuidof(IFsrmExportImport)</code> as the interface identifier. You must use the 
    <b>CLSCTX_INPROC_SERVER</b> class context to create the object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmExportImport</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmExportImport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFsrmExportImport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmexportimport-exportfilegroups">ExportFileGroups</a>
</td>
<td align="left" width="63%">
Exports one or more file groups to the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmexportimport-exportfilescreentemplates">ExportFileScreenTemplates</a>
</td>
<td align="left" width="63%">
Exports one or more file screen templates to the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmexportimport-exportquotatemplates">ExportQuotaTemplates</a>
</td>
<td align="left" width="63%">
Exports one or more quota templates to the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmexportimport-importfilegroups">ImportFileGroups</a>
</td>
<td align="left" width="63%">
Imports one or more file groups from the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmexportimport-importfilescreentemplates">ImportFileScreenTemplates</a>
</td>
<td align="left" width="63%">
Imports one or more file screen templates from the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmexportimport-importquotatemplates">ImportQuotaTemplates</a>
</td>
<td align="left" width="63%">
Imports one or more quota templates from the specified file.

</td>
</tr>
</table> 


## -remarks



Typically, these methods are used to move objects from one computer to another. These methods differ from the 
    import and export methods on the objects (for example, 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroupmanager-exportfilegroups">IFsrmFileGroupManager::ExportFileGroups</a>) 
    in that they write to and read from a file whereas the object methods write to and read from a string.

The file that the export methods create is written in the context of the user.

To create this object from a script, use the <code>Fsrm.FsrmExportImport</code> 
    program identifier.



