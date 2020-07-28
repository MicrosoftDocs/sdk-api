---
UID: NF:directxpackedvector.XMLoadFloat3SE
title: XMLoadFloat3SE function (directxpackedvector.h)
description: Loads an XMFLOAT3SE into an XMVECTOR.
helpviewer_keywords: ["DirectX::PackedVector.XMLoadFloat3SE","XMLoadFloat3SE","XMLoadFloat3SE method [DirectX Math Support APIs]","dxmath.xmloadfloat3se"]
old-location: dxmath\xmloadfloat3se.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadFloat3SE(const XMFLOAT3SE)
ms.date: 12/05/2018
ms.keywords: DirectX::PackedVector.XMLoadFloat3SE, XMLoadFloat3SE, XMLoadFloat3SE method [DirectX Math Support APIs], dxmath.xmloadfloat3se
f1_keywords:
- directxpackedvector/XMLoadFloat3SE
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- directxpackedvector.inl
api_name:
- XMLoadFloat3SE
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMLoadFloat3SE function


## -description


Loads an <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmfloat3se">XMFLOAT3SE</a> into an <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.


## -parameters




### -param pSource [in]

Address of the <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmfloat3se">XMFLOAT3SE</a> structure to load. 


## -returns



Returns an <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.




## -remarks



The following pseudocode demonstrates the operation of the function.


```

  XMVECTOR vectorOut;

  float scale = powf( 2, (float)pSource->e - 15);

  vectorOut.x = ((float)pSource->xm / 512.0f)*scale;
  vectorOut.y = ((float)pSource->ym / 512.0f)*scale;
  vectorOut.z = ((float)pSource->zm / 512.0f)*scale;
  vectorOut.w = 0;

  return vectorOut;

```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>
 

 

