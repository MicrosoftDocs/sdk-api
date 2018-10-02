---
UID: NF:directxpackedvector.XMLoadFloat3PK
title: XMLoadFloat3PK function
author: windows-sdk-content
description: Loads an XMFLOAT3PK into an XMVECTOR.
old-location: dxmath\xmloadfloat3pk.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadFloat3PK(const XMFLOAT3PK)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DirectX::PackedVector.XMLoadFloat3PK, XMLoadFloat3PK, XMLoadFloat3PK method [DirectX Math Support APIs], dxmath.xmloadfloat3pk
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: directxpackedvector.h
req.include-header: DirectXPackedVector.h
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
 - directxpackedvector.inl
api_name:
 - XMLoadFloat3PK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMLoadFloat3PK function


## -description


Loads an <a href="https://msdn.microsoft.com/en-us/library/Ee419478(v=VS.85).aspx">XMFLOAT3PK</a> into an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param pSource [in]

Address of the <a href="https://msdn.microsoft.com/en-us/library/Ee419478(v=VS.85).aspx">XMFLOAT3PK</a> structure to load. 


## -returns



Returns an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.




## -remarks



The following pseudocode demonstrates the operation of the function.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
  XMVECTOR vectorOut;

  float xscale = powf( 2, (float)pSource-&gt;xe - 15);
  vectorOut.x = ((float)pSource-&gt;xm / 64.0f)*xscale;

  float yscale = powf( 2, (float)pSource-&gt;ye - 15);
  vectorOut.y = ((float)pSource-&gt;ym / 64.0f)*yscale;

  float zscale = powf( 2, (float)pSource-&gt;ze - 15);
  vectorOut.z = ((float)pSource-&gt;zm / 32.0f)*zscale;
  
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
 

 

