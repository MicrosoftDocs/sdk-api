---
UID: NS:d3d11.D3D11_TEX2DMS_SRV
title: D3D11_TEX2DMS_SRV
author: windows-driver-content
description: Specifies the subresources from a multisampled 2D texture to use in a shader-resource view.
old-location: direct3d11\d3d11_tex2dms_srv.htm
old-project: direct3d11
ms.assetid: ba896737-a94e-49d0-8f35-2e4ef5a335e7
ms.author: windowsdriverdev
ms.date: 4/6/2018
ms.keywords: D3D11_TEX2DMS_SRV, D3D11_TEX2DMS_SRV structure [Direct3D 11], d3d11/D3D11_TEX2DMS_SRV, dee77306-be03-b837-54e1-859e7d5eb5e1, direct3d11.d3d11_tex2dms_srv
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d11.h
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
req.typenames: D3D11_TEX2DMS_SRV
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D11.h
api_name:
-	D3D11_TEX2DMS_SRV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_TEX2DMS_SRV structure


## -description


Specifies the subresources from a multisampled 2D texture to use in a shader-resource view.


## -struct-fields




### -field UnusedField_NothingToDefine

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Integer of any value. See remarks.


## -remarks



Since a multisampled 2D texture contains a single subresource, there is actually nothing to specify in D3D11_TEX2DMS_RTV. Consequently, <b>UnusedField_NothingToDefine</b> is included so that this structure will compile in C.




## -see-also




<a href="https://msdn.microsoft.com/a29e01ac-8aa1-4a40-ad4d-3b738e129436">Resource Structures</a>
 

 

