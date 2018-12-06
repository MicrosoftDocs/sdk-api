---
UID: NF:directxpackedvector.XMCOLOR.XMCOLOR(uint32_t)
title: XMCOLOR::XMCOLOR(uint32_t)
author: windows-sdk-content
description: Initializes a new instance of XMCOLOR from a uint32_t variable containing component data in a packed format.
old-location: dxmath\xmcolor_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMCOLOR.#ctor(uint32_t)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: XMCOLOR, XMCOLOR constructor [DirectX Math Support APIs], XMCOLOR constructor [DirectX Math Support APIs],XMCOLOR structure, XMCOLOR structure [DirectX Math Support APIs],XMCOLOR constructor, XMCOLOR.XMCOLOR, XMCOLOR.XMCOLOR(uint32_t), XMCOLOR::XMCOLOR, XMCOLOR::XMCOLOR(uint32_t), dxmath.xmcolor_ctor_2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - DirectXPackedVector.h
api_name:
 - XMCOLOR.XMCOLOR
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMCOLOR::XMCOLOR(uint32_t)


## -description


Initializes a new instance of <code>XMCOLOR</code> from a <code>uint32_t</code> variable containing
	component data in a packed format.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/B799AA06-C51B-440A-93AD-3D3334449E27">XMCOLOR</a> from a
	<code>uint32_t</code> variable containing component data in a packed format.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param Color

The values of four color components in a packed format.
	    


## -remarks



The values defining the four components of the new instance of <code>XMCOLOR</code> are
	    stored in the argument <code>Packed</code> as follows:
	

<ul>
<li>
The first 8 bits (bits 0-7) of <b>Packed</b> assigned, as an unsigned
		    integer, to the <b>a</b> member (alpha channel) of the instance of
		    <code>XMCOLOR</code> constructed.
		

</li>
<li>
The second 8 bits (bits 8-15) of <b>Packed</b> assigned, as an unsigned
		    integer, to the <b>r</b> member (red color channel) of the instance of
		    <code>XMCOLOR</code> constructed.
		

</li>
<li>
The third 8 bits (bits 16-23) of <b>Packed</b> assigned, as an unsigned
		    integer, to the <b>g</b> member (green color channel) of the instance of
		    <code>XMCOLOR</code> constructed.
		

</li>
<li>
The fourth 8 bits (bits 24-31) of <b>Packed</b> assigned, as an unsigned
		    integer, to the <b>b</b> member (blue color channel) of the instance of
		    <code>XMCOLOR</code> constructed.
		

</li>
</ul>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/B799AA06-C51B-440A-93AD-3D3334449E27">XMCOLOR</a>



<a href="https://msdn.microsoft.com/9d700016-8a5c-4699-b9cb-f9e91296a2a7">XMCOLOR Constructors</a>
 

 

