---
UID: NF:directxmath.XMVectorSetByIndex
title: XMVectorSetByIndex function
author: windows-sdk-content
description: Use a floating-point object to set the value of one of the four components of an XMVECTOR Data Type containing integer data referenced by an index.
old-location: dxmath\xmvectorsetbyindex.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.accessors.XMVectorSetByIndex(XMVECTOR,float,size_t)
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Use DirectX..XMVectorSetByIndex, XMVectorSetByIndex, XMVectorSetByIndex method [DirectX Math Support APIs], dxmath.xmvectorsetbyindex
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
 - XMVectorSetByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorSetByIndex function


## -description


Use a floating-point object to set the value of one of the four components of an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR Data Type</a> containing
  integer data referenced by an index.


## -parameters




### -param V

A <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR Data Type</a> containing integer data.


### -param f

The floating point value used to set the <i>i</i> component of the returned <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR Data Type</a>.


### -param i

The index of the component to be retrieved.


## -returns



An instance of <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR Data Type</a> whose <i>i</i> component has been set to the floating-point value
       provided by the argument <i>f</i>. All other components of the returned <b>XMVECTOR Data Type</b> instance
       have the same value as those of the input vector <i>V</i>.




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



<a href="https://msdn.microsoft.com/ea5f461f-492c-4b9c-9b89-650c19bf6764">XMVectorGetByIndex</a>



<a href="https://msdn.microsoft.com/f5d80f99-199f-46c4-96d7-a2d86fda48cf">XMVectorSetByIndexPtr</a>
 

 

