---
UID: NF:directxmath.XMVectorGetByIndex
title: XMVectorGetByIndex function (directxmath.h)
author: windows-sdk-content
description: Retrieve the value of one of the four components of an XMVECTOR Data Type containing floating-point data by index.
old-location: dxmath\xmvectorgetbyindex.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.accessors.XMVectorGetByIndex(XMVECTOR,size_t)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorGetByIndex, XMVectorGetByIndex, XMVectorGetByIndex method [DirectX Math Support APIs], dxmath.xmvectorgetbyindex
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
 - XMVectorGetByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorGetByIndex function


## -description


Retrieve the value of one of the four components of an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR Data Type</a> containing floating-point data by
  index.


## -parameters




### -param V

A <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR Data Type</a> containing integer data.


### -param i

The index of the component to be retrieved.


## -returns



The floating-point value of the selected component.




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



<a href="https://msdn.microsoft.com/en-us/library/Hh404787(v=VS.85).aspx">XMVectorGetByIndexPtr</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh404810(v=VS.85).aspx">XMVectorSetByIndex</a>
 

 

