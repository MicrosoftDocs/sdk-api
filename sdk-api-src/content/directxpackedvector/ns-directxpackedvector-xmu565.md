---
UID: NS:directxpackedvector.XMU565
title: XMU565 (directxpackedvector.h)
author: windows-sdk-content
description: A 3D vector with x- and z- components represented as 5-bit unsigned integer values, and the y- component as a 6-bit unsigned integer value.
old-location: dxmath\xmu565.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMU565
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: XMU565, XMU565 structure [DirectX Math Support APIs], directxpackedvector/XMU565, dxmath.xmu565
ms.topic: struct
f1_keywords: 
 - "directxpackedvector/XMU565"
dev_langs:
 - c++
req.header: directxpackedvector.h
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
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectXPackedVector.h
api_name:
 - XMU565
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMU565 structure


## -description


A 3D vector with x- and z- components represented as 5-bit unsigned integer values, 
    and the y- component as a 6-bit unsigned integer value.

For a list of more functionality such as constructors and operators that are available
	using <code>XMU565</code> when you are programming in C++, see <a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xmu565-extensions">XMU565 Extensions</a>.


## -struct-fields




### -field x

 


### -field y

 


### -field z

 


### -field v

Unsigned short representing the 3D vector.
		    


### -field XMU565

TBD 


### -field operator uint16_t

TBD 


### -field operator=

TBD 




#### - x : 5

The 5-bit x component.
			


#### - y : 6

The 5-bit y component.
			


#### - z : 5

The 5-bit z component.
			


## -remarks



You can use <a href="https://docs.microsoft.com/en-us/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmloadu565">XMLoadU565</a> to load <code>XMU565</code> into instances 
      of <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type"> XMVECTOR</a>.
	

You can use <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmstoreu565">XMStoreU565</a> to store instances of <code>XMVECTOR</code> 
    into an instance of <code>XMU565</code>.
	

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xmu565-extensions">XMU565 Extensions</a>
 

 

