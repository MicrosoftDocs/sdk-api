---
UID: NF:directxmath.XMVectorSplatConstant
title: XMVectorSplatConstant function
author: windows-sdk-content
description: Creates a vector with identical floating-point components. Each component is a constant divided by two raised to an integer exponent.
old-location: dxmath\xmvectorsplatconstant.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.initialization.XMVectorSplatConstant(uint32_t,uint32_t)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Use DirectX..XMVectorSplatConstant, XMVectorSplatConstant, XMVectorSplatConstant method [DirectX Math Support APIs], dxmath.xmvectorsplatconstant
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
 - XMVectorSplatConstant
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorSplatConstant function


## -description


Creates a vector with identical floating-point components. Each component is a constant divided by two raised to an
  integer exponent.


## -parameters




### -param IntConstant [in]

This value will be converted to a floating-point number and divided by two raised to the <i>DivExponent</i> power.
        The result is replicated to each component of the returned vector.

The value of <i>IntConstant</i> must satisfy: -16 &lt;= <i>IntConstant</i> &lt;=15.

<div class="alert"><b>Note</b>  This parameter must be a number (an immediate value) and not a variable.</div>
<div> </div>

### -param DivExponent [in]

Describes the exponent applied to the quotient. This parameter must be a number (an immediate value) and not a
        variable.


## -returns



Returns an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> with identical floating-point components. Each component is a constant
       divided by two raised to an integer exponent.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/862a1a83-2371-9885-20d4-184aae52fd10">Vector Initialization Functions</a>



<a href="https://msdn.microsoft.com/a0353e31-d847-4f11-bb6a-fd06999cdbd8">XMVectorSetBinaryConstant</a>



<a href="https://msdn.microsoft.com/d611c895-1b52-410e-8e1b-5f6b70cf6be7">XMVectorSetInt</a>



<a href="https://msdn.microsoft.com/7e7029de-e0b0-43f4-997e-91c70deb4f71">XMVectorSplatConstantInt</a>
 

 

