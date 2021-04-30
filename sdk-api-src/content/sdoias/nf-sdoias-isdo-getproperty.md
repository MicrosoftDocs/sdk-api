---
UID: NF:sdoias.ISdo.GetProperty
title: ISdo::GetProperty (sdoias.h)
description: The GetProperty method retrieves the value of the specified property.
helpviewer_keywords: ["GetProperty","GetProperty method [Network Policy Server]","GetProperty method [Network Policy Server]","ISdo interface","ISdo interface [Network Policy Server]","GetProperty method","ISdo.GetProperty","ISdo::GetProperty","_sdo_isdo_getproperty","nps.SDO_isdo_getproperty","sdo.isdo_getproperty","sdoias/ISdo::GetProperty"]
old-location: nps\SDO_isdo_getproperty.htm
tech.root: Nps
ms.assetid: 9567e731-4240-4b37-8757-2e25824bba0a
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [Network Policy Server], GetProperty method [Network Policy Server],ISdo interface, ISdo interface [Network Policy Server],GetProperty method, ISdo.GetProperty, ISdo::GetProperty, _sdo_isdo_getproperty, nps.SDO_isdo_getproperty, sdo.isdo_getproperty, sdoias/ISdo::GetProperty
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Iassdo.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISdo::GetProperty
 - sdoias/ISdo::GetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdo.GetProperty
---

# ISdo::GetProperty


## -description

The 
<b>GetProperty</b> method retrieves the value of the specified property.

## -parameters

### -param Id [in]

Specifies the ID of an existing property.

### -param pValue [out]

Pointer to a 
<a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> that contains the value of the property.

## -returns

If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.

## -see-also

<a href="/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties">IASCOMMONPROPERTIES</a>



<a href="/windows/desktop/api/sdoias/nn-sdoias-isdo">ISdo</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty">ISdo::SetProperty</a>



<a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a>