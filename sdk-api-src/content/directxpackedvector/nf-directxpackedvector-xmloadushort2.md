---
UID: NF:directxpackedvector.XMLoadUShort2
title: XMLoadUShort2 function (directxpackedvector.h)
author: windows-sdk-content
description: Loads an XMUSHORT2 into an XMVECTOR.
old-location: dxmath\xmloadushort2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadUShort2(const XMUSHORT2)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMLoadUShort2, XMLoadUShort2, XMLoadUShort2 method [DirectX Math Support APIs], dxmath.xmloadushort2
ms.topic: function
f1_keywords: 
 - "directxpackedvector/XMLoadUShort2"
dev_langs:
 - c++
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
req.namespace: Use DirectX.
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
 - XMLoadUShort2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMLoadUShort2 function


## -description


Loads an <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmushort2">XMUSHORT2</a> into an <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.


## -parameters




### -param pSource [in]

Address of the <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmushort2">XMUSHORT2</a> structure to load. This parameter must point to cached
        memory.


## -returns



Returns an <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.




## -remarks



The following pseudocode shows you the operation of the function.


```
XMVECTOR vectorOut;

vectorOut.x = (float)pSource->x;
vectorOut.y = (float)pSource->y;
vectorOut.z = 0;
vectorOut.w = 0;
	
return vectorOut;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-load">DirectXMath Library Vector Load Functions</a>
 

 

