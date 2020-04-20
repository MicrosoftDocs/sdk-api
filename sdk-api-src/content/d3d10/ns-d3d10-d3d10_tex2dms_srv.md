---
UID: NS:d3d10.D3D10_TEX2DMS_SRV
title: D3D10_TEX2DMS_SRV (d3d10.h)
description: Specifies the subresource(s) from a multisampled 2D texture to use in a shader-resource view.helpviewer_keywords: ["85d08460-6071-fabd-5910-b60baa79e1e6","D3D10_TEX2DMS_SRV","D3D10_TEX2DMS_SRV structure [Direct3D 10]","d3d10/D3D10_TEX2DMS_SRV","direct3d10.d3d10_tex2dms_srv"]
old-location: direct3d10\d3d10_tex2dms_srv.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_tex2dms_srv.htm
ms.date: 12/05/2018
ms.keywords: 85d08460-6071-fabd-5910-b60baa79e1e6, D3D10_TEX2DMS_SRV, D3D10_TEX2DMS_SRV structure [Direct3D 10], d3d10/D3D10_TEX2DMS_SRV, direct3d10.d3d10_tex2dms_srv
f1_keywords:
- d3d10/D3D10_TEX2DMS_SRV
dev_langs:
- c++
req.header: d3d10.h
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
- D3D10.h
api_name:
- D3D10_TEX2DMS_SRV
targetos: Windows
req.typenames: D3D10_TEX2DMS_SRV
req.redist: 
ms.custom: 19H1
---

# D3D10_TEX2DMS_SRV structure


## -description


Specifies the <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresource(s)</a> from a multisampled <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">2D texture</a> to use in a shader-resource view.


## -struct-fields




### -field UnusedField_NothingToDefine

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Integer of any value. See remarks.


## -remarks



Since a multisampled 2D texture contains a single subresource, there is actually nothing to specify in <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ns-d3d10-d3d10_tex2dms_rtv">D3D10_TEX2DMS_RTV</a>. Consequently, <b>UnusedField_NothingToDefine</b> is included so that this structure will compile in C.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures">Resource Structures</a>
 

 

