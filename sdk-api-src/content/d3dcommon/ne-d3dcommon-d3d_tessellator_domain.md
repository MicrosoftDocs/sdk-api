---
UID: NE:d3dcommon.D3D_TESSELLATOR_DOMAIN
title: D3D_TESSELLATOR_DOMAIN
author: windows-sdk-content
description: Domain options for tessellator data.
old-location: direct3d11\d3d11_tessellator_domain.htm
old-project: direct3d11
ms.assetid: d0c9ea8a-a1e2-44c3-a4ac-bdc43e5171b5
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: D3D11_TESSELLATOR_DOMAIN, D3D11_TESSELLATOR_DOMAIN enumeration [Direct3D 11], D3D11_TESSELLATOR_DOMAIN_ISOLINE, D3D11_TESSELLATOR_DOMAIN_QUAD, D3D11_TESSELLATOR_DOMAIN_TRI, D3D11_TESSELLATOR_DOMAIN_UNDEFINED, D3D_TESSELLATOR_DOMAIN, b9d735b7-3708-663e-40ab-0d0f519b8b89, d3d11shader/D3D11_TESSELLATOR_DOMAIN, d3d11shader/D3D11_TESSELLATOR_DOMAIN_ISOLINE, d3d11shader/D3D11_TESSELLATOR_DOMAIN_QUAD, d3d11shader/D3D11_TESSELLATOR_DOMAIN_TRI, d3d11shader/D3D11_TESSELLATOR_DOMAIN_UNDEFINED, d3dcommon/D3D11_TESSELLATOR_DOMAIN, d3dcommon/D3D11_TESSELLATOR_DOMAIN_ISOLINE, d3dcommon/D3D11_TESSELLATOR_DOMAIN_QUAD, d3dcommon/D3D11_TESSELLATOR_DOMAIN_TRI, d3dcommon/D3D11_TESSELLATOR_DOMAIN_UNDEFINED, direct3d11.d3d11_tessellator_domain
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3dcommon.h
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
tech.root: 
req.typenames: D3D_TESSELLATOR_DOMAIN
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11Shader.h
 - d3dcommon.h
api_name:
 - D3D11_TESSELLATOR_DOMAIN
product: Windows
targetos: Windows
req.lib: D3d9.lib
req.dll: 
req.irql: 
---

# D3D_TESSELLATOR_DOMAIN enumeration


## -description


Domain options for tessellator data.


## -enum-fields




### -field D3D_TESSELLATOR_DOMAIN_UNDEFINED


### -field D3D_TESSELLATOR_DOMAIN_ISOLINE


### -field D3D_TESSELLATOR_DOMAIN_TRI


### -field D3D_TESSELLATOR_DOMAIN_QUAD


### -field D3D11_TESSELLATOR_DOMAIN_UNDEFINED

The data type is undefined.


### -field D3D11_TESSELLATOR_DOMAIN_ISOLINE

Isoline data.


### -field D3D11_TESSELLATOR_DOMAIN_TRI

Triangle data.


### -field D3D11_TESSELLATOR_DOMAIN_QUAD

Quad data.


## -remarks



The data domain defines the type of data. This enumeration is used by <a href="https://msdn.microsoft.com/25c8f773-e319-4ba1-b332-d45b8323e8c8">D3D11_SHADER_DESC</a>.

The <b>D3D11_TESSELLATOR_DOMAIN</b>     enumeration is type defined in the  D3D11Shader.h header file as a <a href="https://msdn.microsoft.com/9a62f3f4-b9d9-4aed-952e-00f3ad6aafd1">D3D_TESSELLATOR_DOMAIN</a> enumeration, which is fully defined in the  D3DCommon.h header file.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef D3D_TESSELLATOR_DOMAIN D3D11_TESSELLATOR_DOMAIN;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/068ce652-8596-4492-992c-658d1fcf8a2c">Shader Enumerations</a>
 

 

