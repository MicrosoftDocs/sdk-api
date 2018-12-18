---
UID: NE:d3dcommon.D3D_RESOURCE_RETURN_TYPE
title: D3D_RESOURCE_RETURN_TYPE
author: windows-sdk-content
description: Indicates return value type.
old-location: direct3d11\d3d11_resource_return_type.htm
tech.root: direct3d11
ms.assetid: 272f39ae-dc6a-4214-a22f-544764f5b470
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 59063810-740f-d058-3bed-3f66c58da731, D3D11_RESOURCE_RETURN_TYPE, D3D11_RESOURCE_RETURN_TYPE enumeration [Direct3D 11], D3D11_RETURN_TYPE_CONTINUED, D3D11_RETURN_TYPE_DOUBLE, D3D11_RETURN_TYPE_FLOAT, D3D11_RETURN_TYPE_MIXED, D3D11_RETURN_TYPE_SINT, D3D11_RETURN_TYPE_SNORM, D3D11_RETURN_TYPE_UINT, D3D11_RETURN_TYPE_UNORM, D3D_RESOURCE_RETURN_TYPE, d3d11shader/D3D11_RESOURCE_RETURN_TYPE, d3d11shader/D3D11_RETURN_TYPE_CONTINUED, d3d11shader/D3D11_RETURN_TYPE_DOUBLE, d3d11shader/D3D11_RETURN_TYPE_FLOAT, d3d11shader/D3D11_RETURN_TYPE_MIXED, d3d11shader/D3D11_RETURN_TYPE_SINT, d3d11shader/D3D11_RETURN_TYPE_SNORM, d3d11shader/D3D11_RETURN_TYPE_UINT, d3d11shader/D3D11_RETURN_TYPE_UNORM, d3dcommon/D3D11_RESOURCE_RETURN_TYPE, d3dcommon/D3D11_RETURN_TYPE_CONTINUED, d3dcommon/D3D11_RETURN_TYPE_DOUBLE, d3dcommon/D3D11_RETURN_TYPE_FLOAT, d3dcommon/D3D11_RETURN_TYPE_MIXED, d3dcommon/D3D11_RETURN_TYPE_SINT, d3dcommon/D3D11_RETURN_TYPE_SNORM, d3dcommon/D3D11_RETURN_TYPE_UINT, d3dcommon/D3D11_RETURN_TYPE_UNORM, direct3d11.d3d11_resource_return_type
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11shader.h
 - d3dcommon.h
api_name:
 - D3D11_RESOURCE_RETURN_TYPE
product: Windows
targetos: Windows
req.typenames: D3D_RESOURCE_RETURN_TYPE
req.redist: 
---

# D3D_RESOURCE_RETURN_TYPE enumeration


## -description


Indicates return value type.


## -enum-fields




### -field D3D_RETURN_TYPE_UNORM


### -field D3D_RETURN_TYPE_SNORM


### -field D3D_RETURN_TYPE_SINT


### -field D3D_RETURN_TYPE_UINT


### -field D3D_RETURN_TYPE_FLOAT


### -field D3D_RETURN_TYPE_MIXED


### -field D3D_RETURN_TYPE_DOUBLE


### -field D3D_RETURN_TYPE_CONTINUED


### -field D3D10_RETURN_TYPE_UNORM


### -field D3D10_RETURN_TYPE_SNORM


### -field D3D10_RETURN_TYPE_SINT


### -field D3D10_RETURN_TYPE_UINT


### -field D3D10_RETURN_TYPE_FLOAT


### -field D3D10_RETURN_TYPE_MIXED


### -field D3D11_RETURN_TYPE_UNORM

Return type is UNORM.


### -field D3D11_RETURN_TYPE_SNORM

Return type is SNORM.


### -field D3D11_RETURN_TYPE_SINT

Return type is SINT.


### -field D3D11_RETURN_TYPE_UINT

Return type is UINT.


### -field D3D11_RETURN_TYPE_FLOAT

Return type is FLOAT.


### -field D3D11_RETURN_TYPE_MIXED

Return type is unknown.


### -field D3D11_RETURN_TYPE_DOUBLE

Return type is DOUBLE.


### -field D3D11_RETURN_TYPE_CONTINUED

Return type is a multiple-dword type, such as a double or uint64, and the component is continued from the previous component that was declared.  The first component represents the lower bits.


## -remarks



The    <b>D3D11_RESOURCE_RETURN_TYPE</b> enumeration is type defined in the  D3D11shader.h header file as a <a href="https://msdn.microsoft.com/3da3f315-9f92-4557-93b8-94aff42a91fe">D3D_RESOURCE_RETURN_TYPE</a> enumeration, which is fully defined in the  D3DCommon.h header file.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef D3D_RESOURCE_RETURN_TYPE D3D11_RESOURCE_RETURN_TYPE;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/068ce652-8596-4492-992c-658d1fcf8a2c">Shader Enumerations</a>
 

 

