---
UID: NN:fsrm.IFsrmPathMapper
title: IFsrmPathMapper (fsrm.h)
description: Used to retrieve the network share paths that are mapped to a local path.
helpviewer_keywords: ["IFsrmPathMapper","IFsrmPathMapper interface [File Server Resource Manager]","IFsrmPathMapper interface [File Server Resource Manager]","described","fs.ifsrmpathmapper","fsrm.ifsrmpathmapper","fsrm/IFsrmPathMapper"]
old-location: fsrm\ifsrmpathmapper.htm
tech.root: fsrm
ms.assetid: 04e62a10-1719-454b-adfb-6320e31c7a88
ms.date: 12/05/2018
ms.keywords: IFsrmPathMapper, IFsrmPathMapper interface [File Server Resource Manager], IFsrmPathMapper interface [File Server Resource Manager],described, fs.ifsrmpathmapper, fsrm.ifsrmpathmapper, fsrm/IFsrmPathMapper
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
 - IFsrmPathMapper
 - fsrm/IFsrmPathMapper
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
 - IFsrmPathMapper
---

# IFsrmPathMapper interface


## -description

Used to retrieve the network share paths that are mapped to a local path.

To get this interface, call the 
    <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmPathMapper</b> as the class identifier and 
    <code>__uuidof(IFsrmPathMapper)</code> as the interface identifier.

## -inheritance

The <b>IFsrmPathMapper</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmPathMapper</b> also has these types of members:

## -remarks

To create this object from a script, use the program identifier, "Fsrm.FsrmPathMapper".

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/fsrm/fsrmpathmapper">FsrmPathMapper</a>
