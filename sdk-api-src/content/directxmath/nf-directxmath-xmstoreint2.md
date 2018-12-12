---
UID: NF:directxmath.XMStoreInt2
title: XMStoreInt2 function
author: windows-sdk-content
description: Stores an XMVECTOR in a 2-element uint32_t array.
old-location: dxmath\xmstoreint2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreInt2(VOID@,XMVERTORI)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Use DirectX..XMStoreInt2, XMStoreInt2, XMStoreInt2 method [DirectX Math Support APIs], dxmath.xmstoreint2
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
 - XMStoreInt2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMStoreInt2 function


## -description


Stores an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> in a 2-element <b>uint32_t</b> array.


## -parameters




### -param pDestination [out]

Address at which to store the data. This pointer must be 4-byte aligned.


### -param V [in]

Vector containing the data to store.


## -returns



None.




## -remarks



The following pseudocode shows you the operation of the function.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>uint32_t* pElement = (uint32_t*)pDestination;

assert(pDestination);
assert(((uint32_t_PTR)pDestination &amp; 3) == 0);

pElement[0] = V.u[0];
pElement[1] = V.u[1];</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/0e7b66bd-bdb0-956d-2962-b33ae52b3016">DirectXMath Library Vector Store Functions</a>



<a href="https://msdn.microsoft.com/41e10329-9f6f-446f-9640-6c1d65e20cb5">XMINT2</a>



<a href="https://msdn.microsoft.com/c7924ca9-71b9-47fd-bfb2-998f28e2427b">XMStoreSInt2</a>



<a href="https://msdn.microsoft.com/69460147-3abe-4412-bbf2-184e60c65534">XMStoreUInt2</a>



<a href="https://msdn.microsoft.com/33240440-20A8-4320-AF2F-40BA287CB107">XMUINT2</a>
 

 

