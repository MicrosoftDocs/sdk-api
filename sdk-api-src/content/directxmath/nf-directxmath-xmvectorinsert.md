---
UID: NF:directxmath.XMVectorInsert
title: XMVectorInsert function
author: windows-sdk-content
description: Rotates a vector left by a given number of 32-bit components and insert selected elements of that result into another vector.
old-location: dxmath\xmvectorinsert.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.component-wise.XMVectorInsert(XMVECTOR,XMVECTOR,uint32_t,uint32_t,uint32_t,uint32_t,uint32_t)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Use DirectX..XMVectorInsert, XMVectorInsert, XMVectorInsert method [DirectX Math Support APIs], dxmath.xmvectorinsert
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: directxmath.h
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
 - directxmathvector.inl
api_name:
 - XMVectorInsert
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorInsert function


## -description


Rotates a vector left by a given number of 32-bit components and insert selected elements of that result into another
  vector.


## -parameters




### -param VD [in]

Vector to insert into.


### -param VS [in]

Vector to rotate left.


### -param VSLeftRotateElements [in]

Number of 32-bit components by which to rotate <i>VS</i> left.


### -param Select0 [in]

Either 0 or 1. If one, the x-component of the rotated vector will be inserted into the corresponding component of
        <i>VD</i>. Otherwise, the x-component of <i>VD</i> is left alone.


### -param Select1 [in]

Either 0 or 1. If one, the y-component of the rotated vector will be inserted into the corresponding component of
        <i>VD</i>. Otherwise, the y-component of <i>VD</i> is left alone.


### -param Select2 [in]

Either 0 or 1. If one, the z-component of the rotated vector will be inserted into the corresponding component of
        <i>VD</i>. Otherwise, the z-component of <i>VD</i> is left alone.


### -param Select3 [in]

Either 0 or 1. If one, the w-component of the rotated vector will be inserted into the corresponding component of
        <i>VD</i>. Otherwise, the w-component of <i>VD</i> is left alone.


## -returns



Returns the <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> that results from the rotation and insertion.




## -remarks



For best performance, the result of
   <b>XMVectorInsert</b>should be assigned back to <i>VD</i>.

For cases with constant uint32_t parameters, it is more efficent to use the template form of <a href="https://msdn.microsoft.com/d96248a6-35ef-4d37-a929-ac7ea00a6d08">XMVectorInsert</a>:


```

template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3>
    XMVECTOR XMVectorInsert(FXMVECTOR VD, FXMVECTOR VS)
   
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/f5464614-f6bb-427d-5488-3ba0fd4c6e8d">Component-Wise Vector Functions</a>



<a href="https://msdn.microsoft.com/212c9381-6bde-4a09-9710-e2e3fe54f405">XMVectorPermute</a>



<a href="https://msdn.microsoft.com/e12f6450-683d-431f-98d3-324b6c5cdf8f">XMVectorRotateLeft</a>



<a href="https://msdn.microsoft.com/ea47a1a6-6f59-4933-99b1-1b4a67038a6e">XMVectorRotateRight</a>



<a href="https://msdn.microsoft.com/0d0a0795-1eb6-4189-8307-52deeb99a4ba">XMVectorShiftLeft</a>
 

 

