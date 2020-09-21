---
UID: NF:directxpackedvector.XMLoadFloat3PK
title: XMLoadFloat3PK function (directxpackedvector.h)
description: Loads an XMFLOAT3PK into an XMVECTOR.
helpviewer_keywords: ["DirectX::PackedVector.XMLoadFloat3PK","XMLoadFloat3PK","XMLoadFloat3PK method [DirectX Math Support APIs]","dxmath.xmloadfloat3pk"]
old-location: dxmath\xmloadfloat3pk.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadFloat3PK(const XMFLOAT3PK)
ms.date: 12/05/2018
ms.keywords: DirectX::PackedVector.XMLoadFloat3PK, XMLoadFloat3PK, XMLoadFloat3PK method [DirectX Math Support APIs], dxmath.xmloadfloat3pk
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
 - XMLoadFloat3PK
 - directxpackedvector/XMLoadFloat3PK
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
 - XMLoadFloat3PK
---

# XMLoadFloat3PK function


## -description

Loads an <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk">XMFLOAT3PK</a> into an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.

## -parameters

### -param pSource [in]

Address of the <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk">XMFLOAT3PK</a> structure to load.

## -returns

Returns an <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.

## -remarks

The following pseudocode demonstrates the operation of the function.


```

  XMVECTOR vectorOut;

  float xscale = powf( 2, (float)pSource->xe - 15);
  vectorOut.x = ((float)pSource->xm / 64.0f)*xscale;

  float yscale = powf( 2, (float)pSource->ye - 15);
  vectorOut.y = ((float)pSource->ym / 64.0f)*yscale;

  float zscale = powf( 2, (float)pSource->ze - 15);
  vectorOut.z = ((float)pSource->zm / 32.0f)*zscale;
  
  vectorOut.w = 0;

  return vectorOut;

```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>