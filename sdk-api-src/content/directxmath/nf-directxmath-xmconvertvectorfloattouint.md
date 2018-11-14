---
UID: NF:directxmath.XMConvertVectorFloatToUInt
title: XMConvertVectorFloatToUInt function
author: windows-sdk-content
description: Converts an XMVECTOR with float components to an XMVECTOR with uint32_t components and applies a uniform bias.
old-location: dxmath\xmconvertvectorfloattouint.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.conversion.XMConvertVectorFloatToUInt(XMVECTOR,uint32_t)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMConvertVectorFloatToUInt, XMConvertVectorFloatToUInt, XMConvertVectorFloatToUInt method [DirectX Math Support APIs], dxmath.xmconvertvectorfloattouint
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
 - XMConvertVectorFloatToUInt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMConvertVectorFloatToUInt
: 
---

# XMConvertVectorFloatToUInt function


## -description


Converts an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> with <b>float</b> components to an
  <b>XMVECTOR</b> with <b>uint32_t</b> components and applies a uniform bias.


## -parameters




### -param VFloat [in]

Vector with <b>float</b> components that is to be converted.


### -param MulExponent [in]

Each component of <i>VFloat</i> will be converted to a <b>int32_t</b> and then multiplied by two raised to the
        <i>DivExponent</i> power. This parameter must be a number (an immediate value) and not a variable.


## -returns



Returns the converted vector, where each component has been multiplied by two raised to the <i>MulExponent</i>power.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/6a0a8422-991d-00aa-0fd7-b41387adc72e">DirectXMath Library Conversion Functions</a>



<a href="https://msdn.microsoft.com/0642e272-63a1-4595-a6ca-0ec77af01559">XMConvertVectorFloatToInt</a>



<a href="https://msdn.microsoft.com/7f93353d-a00b-47a5-b7cb-99b1e79a51f1">XMConvertVectorUIntToFloat</a>
 

 

