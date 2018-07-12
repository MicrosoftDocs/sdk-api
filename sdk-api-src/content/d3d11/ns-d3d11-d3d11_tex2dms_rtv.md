---
UID: NS:d3d11.D3D11_TEX2DMS_RTV
title: D3D11_TEX2DMS_RTV
author: windows-sdk-content
description: Specifies the subresource from a multisampled 2D texture to use in a render-target view.
old-location: direct3d11\d3d11_tex2dms_rtv.htm
old-project: direct3d11
ms.assetid: 5414183c-4abf-4030-a148-ade5c9213635
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: D3D11_TEX2DMS_RTV, D3D11_TEX2DMS_RTV structure [Direct3D 11], b5ca8db8-f65e-f182-293c-40214b3b3994, d3d11/D3D11_TEX2DMS_RTV, direct3d11.d3d11_tex2dms_rtv
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D11_TEX2DMS_RTV
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_TEX2DMS_RTV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_TEX2DMS_RTV structure


## -description


Specifies the subresource from a multisampled 2D texture to use in a render-target view.


## -struct-fields




### -field UnusedField_NothingToDefine

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Integer of any value. See remarks.


## -remarks



Since a multisampled 2D texture contains a single subresource, there is actually nothing to specify in D3D11_TEX2DMS_RTV. Consequently, <b>UnusedField_NothingToDefine</b> is included so that this structure will compile in C.




## -see-also




<a href="https://msdn.microsoft.com/a29e01ac-8aa1-4a40-ad4d-3b738e129436">Resource Structures</a>
 

 

