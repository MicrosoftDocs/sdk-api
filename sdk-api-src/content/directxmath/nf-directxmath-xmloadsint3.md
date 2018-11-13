---
UID: NF:directxmath.XMLoadSInt3
title: XMLoadSInt3 function
author: windows-sdk-content
description: Loads signed integer data into the x, y, and z components of an XMVECTOR.
old-location: dxmath\xmloadsint3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadSInt3(const XMINT3)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMLoadSInt3, XMLoadSInt3, XMLoadSInt3 method [DirectX Math Support APIs], dxmath.xmloadsint3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: directxmath.h
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
 - DirectXMath.h
api_name:
 - XMLoadSInt3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMLoadSInt3 function


## -description


Loads signed integer data into the x, y, and z components 
  of an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param pSource [in]

Address of an <a href="https://msdn.microsoft.com/9924ed70-e6f8-4040-aab1-977bc3f197e6">XMINT3</a> structure containing the data to load. 
        


## -returns



Returns an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> loaded with the data from the <i>pSource</i>parameter.




## -remarks



For 16-byte aligned memory, it may be faster to use <a href="https://msdn.microsoft.com/689065df-18f6-444a-aa24-bd2ae5bccd1b">XMLoadInt3A</a> 
    with a casting operator.

The following pseudocode shows the operation of this function.


```

XMVECTOR vectorOut;

vectorOut.x = (float)pSource->x;
vectorOut.y = (float)pSource->y;
vectorOut.z = (float)pSource->z;
vectorOut.w = 0;

return vectorOut;
    
    
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>
 

 

