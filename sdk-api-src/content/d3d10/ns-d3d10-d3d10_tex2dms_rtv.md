---
UID: NS:d3d10.D3D10_TEX2DMS_RTV
title: D3D10_TEX2DMS_RTV
author: windows-sdk-content
description: Specifies the subresource from a multisampled 2D texture to use in a render-target view.
old-location: direct3d10\d3d10_tex2dms_rtv.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_tex2dms_rtv.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D10_TEX2DMS_RTV, D3D10_TEX2DMS_RTV structure [Direct3D 10], b35fccdd-d7a7-672b-7f33-80eef15788d6, d3d10/D3D10_TEX2DMS_RTV, direct3d10.d3d10_tex2dms_rtv
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
 - D3D10_TEX2DMS_RTV
product: Windows
targetos: Windows
req.typenames: D3D10_TEX2DMS_RTV
req.redist: 
---

# D3D10_TEX2DMS_RTV structure


## -description


Specifies the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">subresource</a> from a multisampled <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">2D texture</a> to use in a render-target view.


## -struct-fields




### -field UnusedField_NothingToDefine

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Integer of any value. See remarks.


## -remarks



Since a multisampled 2D texture contains a single subresource, there is actually nothing to specify in <b>D3D10_TEX2DMS_RTV</b>. Consequently, <b>UnusedField_NothingToDefine</b> is included so that this structure will compile in C.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205277(v=VS.85).aspx">Resource Structures</a>
 

 

