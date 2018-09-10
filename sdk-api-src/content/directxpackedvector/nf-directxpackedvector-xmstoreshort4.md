---
UID: NF:directxpackedvector.XMStoreShort4
title: XMStoreShort4 function
author: windows-sdk-content
description: Stores an XMVECTOR in an XMSHORT4.
old-location: dxmath\xmstoreshort4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreShort4(XMSHORT4@,XMVECTOR)
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DirectX::PackedVector.XMStoreShort4, XMStoreShort4, XMStoreShort4 method [DirectX Math Support APIs], dxmath.xmstoreshort4
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - XMStoreShort4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMStoreShort4 function


## -description


Stores an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> in an <a href="https://msdn.microsoft.com/en-us/library/Ee420202(v=VS.85).aspx">XMSHORT4</a>.


## -parameters




### -param pDestination [out]

Address at which to store the data.


### -param V [in]

Vector containing the data to store.


## -returns



None.




## -remarks



This function takes a vector, clamps it to the range -32767.0f to 32767.0f, converts the components into a signed, normalized integer format, and writes the results out to four short integer values at the given address. The most significant component is written to the first two bytes of the address, the next most significant component is written to the next two bytes of the address, and so on.

The following pseudocode demonstrates the operation of the function.


```
static const XMVECTOR  Min = {-32767.0f, -32767.0f, -32767.0f, -32767.0f};
static const XMVECTOR  Max = {32767.0f, 32767.0f, 32767.0f, 32767.0f};
XMVECTOR               N;
N = XMVectorClamp(V, Min, Max);
N = XMVectorRound(N);

pDestination->x = (int16_t)N.x; // 2 bytes to address pDestination
pDestination->y = (int16_t)N.y; // 2 bytes to address (uint8_t*)pDestination + 2
pDestination->z = (int16_t)N.z; // 2 bytes to address (uint8_t*)pDestination + 4
pDestination->w = (int16_t)N.w; // 2 bytes to address (uint8_t*)pDestination + 6
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/0e7b66bd-bdb0-956d-2962-b33ae52b3016">DirectXMath Library Vector Store Functions</a>
 

 

