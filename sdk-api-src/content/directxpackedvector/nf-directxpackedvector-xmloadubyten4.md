---
UID: NF:directxpackedvector.XMLoadUByteN4
title: XMLoadUByteN4 function (directxpackedvector.h)
author: windows-sdk-content
description: Loads an XMUBYTEN4 into an XMVECTOR.
old-location: dxmath\xmloadubyten4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadUByteN4(const XMUBYTEN4)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DirectX::PackedVector.XMLoadUByteN4, XMLoadUByteN4, XMLoadUByteN4 method [DirectX Math Support APIs], dxmath.xmloadubyten4
ms.topic: function
f1_keywords: 
 - "directxpackedvector/XMLoadUByteN4"
req.header: directxpackedvector.h
req.include-header: DirectXMath.h
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
 - directxpackedvector.h
api_name:
 - XMLoadUByteN4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMLoadUByteN4 function


## -description


Loads an <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyten4">XMUBYTEN4</a> into an <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.


## -parameters




### -param pSource [in]

Address of the <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyten4">XMUBYTEN4</a> structure to load. This parameter must point to cached
        memory.


## -returns



Returns an <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.




## -remarks



The following pseudocode demonstrates the operation of the function.


```
XMVECTOR vectorOut;

vectorOut.x = (float)pSource->x / 255.0f;
vectorOut.y = (float)pSource->y / 255.0f;
vectorOut.z = (float)pSource->z / 255.0f;
vectorOut.w = (float)pSource->w / 255.0f;
	
return vectorOut;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>
 

 

