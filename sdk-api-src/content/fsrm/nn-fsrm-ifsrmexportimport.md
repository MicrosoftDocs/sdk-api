---
UID: NN:fsrm.IFsrmExportImport
title: IFsrmExportImport (fsrm.h)
description: Used to export and import FSRM objects.
helpviewer_keywords: ["IFsrmExportImport","IFsrmExportImport interface [File Server Resource Manager]","IFsrmExportImport interface [File Server Resource Manager]","described","fs.ifsrmexportimport","fsrm.ifsrmexportimport","fsrm/IFsrmExportImport"]
old-location: fsrm\ifsrmexportimport.htm
tech.root: fsrm
ms.assetid: 5a3b682e-d2c3-43b3-9d10-4bba9d9c81d4
ms.date: 12/05/2018
ms.keywords: IFsrmExportImport, IFsrmExportImport interface [File Server Resource Manager], IFsrmExportImport interface [File Server Resource Manager],described, fs.ifsrmexportimport, fsrm.ifsrmexportimport, fsrm/IFsrmExportImport
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmExportImport
 - fsrm/IFsrmExportImport
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmExportImport
---

# IFsrmExportImport interface


## -description

Used to export and import FSRM objects.
<div class="alert"><b>Note</b>  This interface supports local use only. Remote operations are not supported.</div><div> </div>To get this interface, call the 
    <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmExportImport</b> as the class identifier and 
    <code>__uuidof(IFsrmExportImport)</code> as the interface identifier. You must use the 
    <b>CLSCTX_INPROC_SERVER</b> class context to create the object.

## -inheritance

The <b>IFsrmExportImport</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmExportImport</b> also has these types of members:

## -remarks

Typically, these methods are used to move objects from one computer to another. These methods differ from the 
    import and export methods on the objects (for example, 
    <a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroupmanager-exportfilegroups">IFsrmFileGroupManager::ExportFileGroups</a>) 
    in that they write to and read from a file whereas the object methods write to and read from a string.

The file that the export methods create is written in the context of the user.

To create this object from a script, use the <code>Fsrm.FsrmExportImport</code> 
    program identifier.
