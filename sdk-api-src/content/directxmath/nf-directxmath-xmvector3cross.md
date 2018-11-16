---
UID: NF:directxmath.XMVector3Cross
title: XMVector3Cross function
author: windows-sdk-content
description: Computes the cross product between two 3D vectors.
old-location: dxmath\xmvector3cross.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector3Cross(XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Use DirectX..XMVector3Cross, XMVector3Cross, XMVector3Cross method [DirectX Math Support APIs], dxmath.xmvector3cross
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
 - XMVector3Cross
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMVector3Cross
: 
---

# XMVector3Cross function


## -description


Computes the cross product between two 3D vectors.


## -parameters




### -param V1 [in]

3D vector.


### -param V2 [in]

3D vector.


## -returns



Returns the cross product of <i>V1</i> and <i>V2</i>.




## -remarks



The following pseudocode demonstrates the operation of the function:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
XMVECTOR Result;
Result.x = (V1.y * V2.z) - (V1.z * V2.y);
Result.y = (V1.z * V2.x) - (V1.x * V2.z);
Result.z = (V1.x * V2.y) - (V1.y * V2.x);
Result.w = 0;
return Result;
    </pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/f2cee697-b4ec-5e4d-a87b-622c9fb7997c">DirectXMath Library 3D Vector Geometric Functions</a>
 

 

