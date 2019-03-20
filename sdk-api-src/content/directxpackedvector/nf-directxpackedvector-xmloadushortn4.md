---
UID: NF:directxpackedvector.XMLoadUShortN4
title: XMLoadUShortN4 function (directxpackedvector.h)
author: windows-sdk-content
description: Loads an XMUSHORTN4 into an XMVECTOR.
old-location: dxmath\xmloadushortn4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadUShortN4(const XMUSHORTN4)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DirectX::PackedVector.XMLoadUShortN4, XMLoadUShortN4, XMLoadUShortN4 method [DirectX Math Support APIs], dxmath.xmloadushortn4
ms.topic: function
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
 - XMLoadUShortN4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMLoadUShortN4 function


## -description


Loads an <a href="https://msdn.microsoft.com/en-us/library/Ee420726(v=VS.85).aspx">XMUSHORTN4</a> into an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param pSource [in]

Address of the <a href="https://msdn.microsoft.com/en-us/library/Ee420726(v=VS.85).aspx">XMUSHORTN4</a> structure to load. This parameter must point to cached
        memory.


## -returns



Returns an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.




## -remarks



The following pseudocode demonstrates the operation of the function.


```
XMVECTOR vectorOut;

vectorOut.x = (float)pSource->x / 65535.0f;
vectorOut.y = (float)pSource->y / 65535.0f;
vectorOut.z = (float)pSource->z / 65535.0f;
vectorOut.w = (float)pSource->w / 65535.0f;
	
return vectorOut;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>
 

 

