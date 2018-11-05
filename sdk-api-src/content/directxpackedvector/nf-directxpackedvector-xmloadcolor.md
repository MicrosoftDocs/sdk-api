---
UID: NF:directxpackedvector.XMLoadColor
title: XMLoadColor function
author: windows-sdk-content
description: Loads an XMCOLOR into an XMVECTOR.
old-location: dxmath\xmloadcolor.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadColor(const XMCOLOR)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DirectX::PackedVector.XMLoadColor, XMLoadColor, XMLoadColor method [DirectX Math Support APIs], dxmath.xmloadcolor
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
 - XMLoadColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMLoadColor function


## -description


Loads an <a href="https://msdn.microsoft.com/B799AA06-C51B-440A-93AD-3D3334449E27">XMCOLOR</a> into an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param pSource [in]

Address of the <a href="https://msdn.microsoft.com/B799AA06-C51B-440A-93AD-3D3334449E27">XMCOLOR</a> structure to load. 


## -returns



Returns an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter with X containing 
	   the Red color channel, Y containing the Green, Z the Blue, and W the Alpha channel. The values in the components range from 0 to 1.




## -remarks



The following pseudocode demonstrates the operation of the function.


```
XMVECTOR vectorOut;

vectorOut.x = (float)((pSource->c >> 16) & 0xFF) / 255.0f;
vectorOut.y = (float)((pSource->c >> 8) & 0xFF) / 255.0f;
vectorOut.z = (float)((pSource->c >> 0) & 0xFF) / 255.0f;
vectorOut.w = (float)((pSource->c >> 24) & 0xFF) / 255.0f;

return vectorOut;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>
 

 

