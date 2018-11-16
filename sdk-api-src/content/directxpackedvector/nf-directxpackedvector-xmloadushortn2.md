---
UID: NF:directxpackedvector.XMLoadUShortN2
title: XMLoadUShortN2 function
author: windows-sdk-content
description: Loads an XMUSHORTN2 into an XMVECTOR.
old-location: dxmath\xmloadushortn2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadUShortN2(const XMUSHORTN2)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Use DirectX..XMLoadUShortN2, XMLoadUShortN2, XMLoadUShortN2 method [DirectX Math Support APIs], dxmath.xmloadushortn2
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - directxpackedvector.h
api_name:
 - XMLoadUShortN2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMLoadUShortN2
: 
---

# XMLoadUShortN2 function


## -description


Loads an <a href="https://msdn.microsoft.com/05f62462-2b6a-4d1b-bf83-9109a254839e">XMUSHORTN2</a> into an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param pSource [in]

Address of the <a href="https://msdn.microsoft.com/05f62462-2b6a-4d1b-bf83-9109a254839e">XMUSHORTN2</a> structure to load. This parameter must point to cached
        memory.


## -returns



Returns an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.




## -remarks



The following pseudocode shows you the operation of the function.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>XMVECTOR vectorOut;

vectorOut.x = (float)pSource-&gt;x / 65535.0f;
vectorOut.y = (float)pSource-&gt;y / 65535.0f;
vectorOut.z = 0;
vectorOut.w = 0;
	
return vectorOut;</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>
 

 

