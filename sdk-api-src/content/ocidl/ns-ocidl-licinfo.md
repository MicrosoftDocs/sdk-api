---
UID: NS:ocidl.tagLICINFO
title: LICINFO (ocidl.h)
description: Contains parameters that describe the licensing behavior of a class factory that supports licensing. The structure is filled by calling the IClassFactory2::GetLicInfo method.
helpviewer_keywords: ["*LPLICINFO","LICINFO","LICINFO structure [COM]","LPLICINFO","LPLICINFO structure pointer [COM]","_ctrl_LICINFO","com.licinfo","ocidl/LICINFO","ocidl/LPLICINFO"]
old-location: com\licinfo.htm
tech.root: com
ms.assetid: a90d82f3-8dc4-4b1d-81f7-9d3a19e74314
ms.date: 12/05/2018
ms.keywords: '*LPLICINFO, LICINFO, LICINFO structure [COM], LPLICINFO, LPLICINFO structure pointer [COM], _ctrl_LICINFO, com.licinfo, ocidl/LICINFO, ocidl/LPLICINFO'
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LICINFO, *LPLICINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLICINFO
 - ocidl/tagLICINFO
 - LPLICINFO
 - ocidl/LPLICINFO
 - LICINFO
 - ocidl/LICINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OCIdl.h
api_name:
 - LICINFO
---

# LICINFO structure


## -description

Contains parameters that describe the licensing behavior of a class factory that supports licensing. The structure is filled by calling the <a href="/windows/desktop/api/ocidl/nf-ocidl-iclassfactory2-getlicinfo">IClassFactory2::GetLicInfo</a> method.

## -struct-fields

### -field cbLicInfo

The size of the structure, in bytes.

### -field fRuntimeKeyAvail

Indicates whether this class factory allows the creation of its objects on an unlicensed machine through the use of a license key. If <b>TRUE</b>, <a href="/windows/desktop/api/ocidl/nf-ocidl-iclassfactory2-requestlickey">IClassFactory2::RequestLicKey</a> can be called to obtain the key. If <b>FALSE</b>, objects can be created only on a fully licensed machine.

### -field fLicVerified

Indicates whether a full machine license exists such that calls to <a href="/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance">IClassFactory::CreateInstance</a> and <a href="/windows/desktop/api/ocidl/nf-ocidl-iclassfactory2-requestlickey">IClassFactory2::RequestLicKey</a> will succeed. If <b>TRUE</b>, the full machine license exists. Thus, objects can be created freely. and a license key is available if <b>fRuntimeKeyAvail</b> is also <b>TRUE</b>. If <b>FALSE</b>, this class factory cannot create any instances of objects on this machine unless the proper license key is passed to <a href="/windows/desktop/api/ocidl/nf-ocidl-iclassfactory2-createinstancelic">IClassFactory2::CreateInstanceLic</a>.

## -see-also

<a href="/windows/desktop/api/ocidl/nf-ocidl-iclassfactory2-getlicinfo">IClassFactory2::GetLicInfo</a>