---
UID: NN:fsrmscreen.IFsrmFileScreenTemplateManager
title: IFsrmFileScreenTemplateManager (fsrmscreen.h)
description: Used to manage file screen templates.
helpviewer_keywords: ["IFsrmFileScreenTemplateManager","IFsrmFileScreenTemplateManager interface [File Server Resource Manager]","IFsrmFileScreenTemplateManager interface [File Server Resource Manager]","described","fs.ifsrmfilescreentemplatemanager","fsrm.ifsrmfilescreentemplatemanager","fsrmscreen/IFsrmFileScreenTemplateManager"]
old-location: fsrm\ifsrmfilescreentemplatemanager.htm
tech.root: fsrm
ms.assetid: 89577ab3-2648-4b37-9fc0-c64929223a13
ms.date: 12/05/2018
ms.keywords: IFsrmFileScreenTemplateManager, IFsrmFileScreenTemplateManager interface [File Server Resource Manager], IFsrmFileScreenTemplateManager interface [File Server Resource Manager],described, fs.ifsrmfilescreentemplatemanager, fsrm.ifsrmfilescreentemplatemanager, fsrmscreen/IFsrmFileScreenTemplateManager
req.header: fsrmscreen.h
req.include-header: FsrmScreen.h, FsrmTlb.h
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
 - IFsrmFileScreenTemplateManager
 - fsrmscreen/IFsrmFileScreenTemplateManager
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
 - IFsrmFileScreenTemplateManager
---

# IFsrmFileScreenTemplateManager interface


## -description

Used to manage file screen templates.

To get this interface, call the 
    <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmFileScreenTemplateManager</b> as the class identifier and 
    <code>__uuidof(IFsrmFileScreenTemplateManager)</code> as the interface 
    identifier. For an example, see 
    <a href="/previous-versions/windows/desktop/fsrm/using-templates-to-define-file-screens">Using Templates to Define File Screens</a>.

## -inheritance

The <b>IFsrmFileScreenTemplateManager</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmFileScreenTemplateManager</b> also has these types of members:

## -remarks

Note that a new installation of the operating system includes FSRM-defined templates.

To create this object from a script, use the "Fsrm.FsrmFileScreenTemplateManager" program 
    identifier.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/fsrm/fsrmfilescreentemplatemanager">FsrmFileScreenTemplateManager</a>
