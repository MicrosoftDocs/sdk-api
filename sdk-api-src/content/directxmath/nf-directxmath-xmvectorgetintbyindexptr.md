---
UID: NF:directxmath.XMVectorGetIntByIndexPtr
title: XMVectorGetIntByIndexPtr function
author: windows-sdk-content
description: Retrieve, into an instance of an integer referenced by pointer, the value of one of the four components of an XMVECTOR Data Type containing integer data by index.
old-location: dxmath\xmvectorgetintbyindexptr.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.accessors.XMVectorGetIntByIndexPtr(uint32_t@,XMVECTOR,size_t)
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: Use DirectX..XMVectorGetIntByIndexPtr, XMVectorGetIntByIndexPtr, XMVectorGetIntByIndexPtr method [DirectX Math Support APIs], dxmath.xmvectorgetintbyindexptr
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
 - XMVectorGetIntByIndexPtr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorGetIntByIndexPtr function


## -description


Retrieve, into an instance of an integer referenced by pointer, the value of one of the four components of an
  <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR Data Type</a> containing integer data by index.


## -parameters




### -param x [out]

Pointer to an instance of an integer object that will receive the value of the <i>i</i> component of the
        <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR Data Type</a> object <code>V</code>.


### -param V

A <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR Data Type</a> containing integer data.


### -param i

The index of the component to be retrieved.


## -returns



None.




## -remarks



The value of <i>i</i> must be positive and less than or equal to three ( <i>0 </i> &lt;= <i> i </i> &lt;=
   <i> 3</i> ).

The indexes have the following correspondence with <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR Data Type</a> vector components:

<table>
<tr>
<th>Index</th>
<th>Component</th>
</tr>
<tr>
<td>
<code>0</code>

</td>
<td>
<code>x</code>

</td>
</tr>
<tr>
<td>
<code>1</code>

</td>
<td>
<code>y</code>

</td>
</tr>
<tr>
<td>
<code>2</code>

</td>
<td>
<code>z</code>

</td>
</tr>
<tr>
<td>
<code>3</code>

</td>
<td>
<code>w</code>

</td>
</tr>
</table>
 

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/6e7453b8-0dee-6fc5-cbac-fe20e4e3ef60">DirectXMath Library Vector Accessor Functions</a>



<a href="https://msdn.microsoft.com/a115bc06-deef-48d9-9a81-825cc2c375e2">XMVectorGetIntByIndex</a>



<a href="https://msdn.microsoft.com/d7641192-3033-4dea-8ee2-9c6a27b784b4">XMVectorSetIntByIndexPtr</a>
 

 

