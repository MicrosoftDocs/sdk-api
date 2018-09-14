---
UID: NN:fsrm.IFsrmExportImport
title: IFsrmExportImport
author: windows-sdk-content
description: Used to export and import FSRM objects.
old-location: fsrm\ifsrmexportimport.htm
tech.root: fsrm
ms.assetid: 5a3b682e-d2c3-43b3-9d10-4bba9d9c81d4
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: IFsrmExportImport, IFsrmExportImport interface [File Server Resource Manager], IFsrmExportImport interface [File Server Resource Manager],described, fs.ifsrmexportimport, fsrm.ifsrmexportimport, fsrm/IFsrmExportImport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmExportImport interface


## -description


Used to export and import FSRM objects.
<div class="alert"><b>Note</b>  This interface supports local use only. Remote operations are not supported.</div><div> </div>To get this interface, call the 
    <a href="_com_CoCreateInstanceEx">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmExportImport</b> as the class identifier and 
    <code>__uuidof(IFsrmExportImport)</code> as the interface identifier. You must use the 
    <b>CLSCTX_INPROC_SERVER</b> class context to create the object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmExportImport</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFsrmExportImport</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/2be3715f-d9c7-4554-9416-a1cc4e512402">ExportFileGroups</a>
</td>
<td align="left" width="63%">
Exports one or more file groups to the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5804dece-7243-4f41-a949-e663852219e8">ExportFileScreenTemplates</a>
</td>
<td align="left" width="63%">
Exports one or more file screen templates to the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ede839ed-3e6f-4b70-bede-07e097ecc1e6">ExportQuotaTemplates</a>
</td>
<td align="left" width="63%">
Exports one or more quota templates to the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8d18971-ba3e-4e20-83ff-1290bc453b90">ImportFileGroups</a>
</td>
<td align="left" width="63%">
Imports one or more file groups from the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea2fbd88-777e-454c-8d32-0d704c219558">ImportFileScreenTemplates</a>
</td>
<td align="left" width="63%">
Imports one or more file screen templates from the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90b70f64-fbc7-48d2-9cf7-71e625ed32af">ImportQuotaTemplates</a>
</td>
<td align="left" width="63%">
Imports one or more quota templates from the specified file.

</td>
</tr>
</table> 


## -remarks



Typically, these methods are used to move objects from one computer to another. These methods differ from the 
    import and export methods on the objects (for example, 
    <a href="https://msdn.microsoft.com/59d7ef32-f06b-4167-8e28-da88da27ab0a">IFsrmFileGroupManager::ExportFileGroups</a>) 
    in that they write to and read from a file whereas the object methods write to and read from a string.

The file that the export methods create is written in the context of the user.

To create this object from a script, use the <code>Fsrm.FsrmExportImport</code> 
    program identifier.



