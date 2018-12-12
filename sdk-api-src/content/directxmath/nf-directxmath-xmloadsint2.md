---
UID: NF:directxmath.XMLoadSInt2
title: XMLoadSInt2 function
author: windows-sdk-content
description: Loads signed integer data into the x and y components of an XMVECTOR.
old-location: dxmath\xmloadsint2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadSInt2(const XMINT2)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Use DirectX..XMLoadSInt2, XMLoadSInt2, XMLoadSInt2 method [DirectX Math Support APIs], dxmath.xmloadsint2
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
 - XMLoadSInt2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMLoadSInt2 function


## -description


Loads signed integer data into the x and y components 
  of an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param pSource [in]

Address of an <a href="https://msdn.microsoft.com/41e10329-9f6f-446f-9640-6c1d65e20cb5">XMINT2</a> structure containing the data to load. 
        


## -returns



Returns an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> loaded with the data from the <i>pSource</i>parameter.




## -remarks



For 16-byte aligned memory, it may be faster to use <a href="https://msdn.microsoft.com/2bf6c9d2-8440-4c2c-9fab-2af3885ccaa6">XMLoadInt2A</a>with a casting operator.

The following pseudocode shows the operation of this function.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
XMVECTOR vectorOut;

vectorOut.x = (float)pSource-&gt;x;
vectorOut.y = (float)pSource-&gt;y;
vectorOut.z = 0;
vectorOut.w = 0;

return vectorOut;
    
    </pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>
 

 

