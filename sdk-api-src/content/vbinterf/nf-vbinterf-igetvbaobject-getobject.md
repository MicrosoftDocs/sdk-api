---
UID: NF:vbinterf.IGetVBAObject.GetObject
title: IGetVBAObject::GetObject (vbinterf.h)
description: Gets a pointer to an interface on the VBA object.
helpviewer_keywords: ["GetObject","GetObject method [COM]","GetObject method [COM]","IGetVBAObject interface","IGetVBAObject interface [COM]","GetObject method","IGetVBAObject.GetObject","IGetVBAObject::GetObject","_com_IGetVBAObject_GetObject","com.igetvbaobject_getobject","vbinterf/IGetVBAObject::GetObject"]
old-location: com\igetvbaobject_getobject.htm
tech.root: com
ms.assetid: 0701c4e7-9a35-42fe-893c-ca898b3716ea
ms.date: 12/05/2018
ms.keywords: GetObject, GetObject method [COM], GetObject method [COM],IGetVBAObject interface, IGetVBAObject interface [COM],GetObject method, IGetVBAObject.GetObject, IGetVBAObject::GetObject, _com_IGetVBAObject_GetObject, com.igetvbaobject_getobject, vbinterf/IGetVBAObject::GetObject
req.header: vbinterf.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGetVBAObject::GetObject
 - vbinterf/IGetVBAObject::GetObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VbInterf.h
api_name:
 - IGetVBAObject.GetObject
---

# IGetVBAObject::GetObject


## -description

Gets a pointer to an interface on the VBA object.
<div class="alert"><b>Note</b>  The use of this method is no longer recommended because containers other than Visual Basic do not support 
    it.</div><div> </div>

## -parameters

### -param riid [in]

Specifies the interface to retrieve. Pass <b>IID_IVBFormat</b> to retrieve a pointer to 
      the <a href="/windows/desktop/api/vbinterf/nn-vbinterf-ivbformat">IVBFormat</a> interface.

### -param ppvObj [out]

Pointer to the interface.

### -param dwReserved [in]

Reserved.

## -returns

This method supports the standard return values <b>E_INVALIDARG</b>, 
      <b>E_OUTOFMEMORY</b>, and <b>E_UNEXPECTED</b>, as well as the 
      following:

## -see-also

<a href="/windows/desktop/api/vbinterf/nn-vbinterf-igetvbaobject">IGetVBAObject</a>