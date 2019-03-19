---
UID: NF:directxpackedvector.XMLoadDecN4
title: XMLoadDecN4 function (directxpackedvector.h)
author: windows-sdk-content
description: Loads an XMDECN4 into an XMVECTOR.
old-location: dxmath\xmloaddecn4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadDecN4(const XMDECN4)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DirectX::PackedVector.XMLoadDecN4, XMLoadDecN4, XMLoadDecN4 method [DirectX Math Support APIs], dxmath.xmloaddecn4
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
 - XMLoadDecN4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMLoadDecN4 function


## -description


Loads an <a href="https://msdn.microsoft.com/en-us/library/Ee419440(v=VS.85).aspx">XMDECN4</a> into an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param pSource [in]

Address of the <a href="https://msdn.microsoft.com/en-us/library/Ee419440(v=VS.85).aspx">XMDECN4</a> structure to load. 


## -returns



Returns an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.




## -remarks



The following pseudocode demonstrates the operation of the function.


```
XMVECTOR vectorOut;

uint32_t Element;
static const uint32_t SignExtend[] = {0x00000000, 0xFFFFFC00};
static const uint32_t SignExtendW[] = {0x00000000, 0xFFFFFFFC};

Element = pSource->v & 0x3FF;
vectorOut.x = (float)(int16_t)(Element | SignExtend[Element >> 9]) / 511.0f;
Element = (pSource->v >> 10) & 0x3FF;
vectorOut.y = (float)(int16_t)(Element | SignExtend[Element >> 9]) / 511.0f;
Element = (pSource->v >> 20) & 0x3FF;
vectorOut.z = (float)(int16_t)(Element | SignExtend[Element >> 9]) / 511.0f;
Element = pSource->v >> 30;
vectorOut.w = (float)(int16_t)(Element | SignExtendW[Element >> 1]);

return vectorOut;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>
 

 

