---
UID: NF:directxpackedvector.XMLoadUDecN4_XR
title: XMLoadUDecN4_XR function (directxpackedvector.h)
description: Loads an extended range XMUDECN4 into an XMVECTOR.
helpviewer_keywords: ["DirectX::PackedVector.XMLoadUDecN4_XR","XMLoadUDecN4_XR","XMLoadUDecN4_XR method [DirectX Math Support APIs]","dxmath._xmloadudecn4_xr"]
old-location: dxmath\_xmloadudecn4_xr.htm
tech.root: dxmath
ms.assetid: C67EEA1C-C416-4E8F-A0D9-F061EF1CD119
ms.date: 12/05/2018
ms.keywords: DirectX::PackedVector.XMLoadUDecN4_XR, XMLoadUDecN4_XR, XMLoadUDecN4_XR method [DirectX Math Support APIs], dxmath._xmloadudecn4_xr
req.header: directxpackedvector.h
req.include-header: DirectXPackedVector.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: DirectX::PackedVector
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
 - XMLoadUDecN4_XR
 - directxpackedvector/XMLoadUDecN4_XR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - directxpackedvector.inl
api_name:
 - XMLoadUDecN4_XR
---

# XMLoadUDecN4_XR function


## -description

Loads an extended range <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmudecn4">XMUDECN4</a> into an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>. This type loads a 10:10:10:2 normalized GPU format using the Extended Range (XR) with the color bias set to match DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM.

## -parameters

### -param pSource [in]

Address of the <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmudecn4">XMUDECN4</a> structure to load.

## -returns

Returns an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.

## -remarks

The following pseudocode demonstrates the operation of the function.


```
XMVECTOR vectorOut;

int32_t Element;

Element = pSource->v & 0x3FF;
vectorOut.x = (float)(Element - 0x180) / 510.f;
Element = (pSource->v >> 10) & 0x3FF;
vectorOut.y = (float)(Element - 0x180) / 510.f;
Element = (pSource->v >> 20) & 0x3FF;
vectorOut.z = (float)(Element - 0x180) / 510.f;
vectorOut.w = (float)(pSource->v >> 30) / 3.f;

return vectorOut;
```


For more details on the Extended Range (XR) with Bias conversion, see <a href="/windows-hardware/drivers/display/xr-bias-color-channel-conversion-rules">XR_BIAS Color Channel Conversion Rules</a>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>



<a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmstoreudecn4_xr">XMStoreUDecN4_XR</a>