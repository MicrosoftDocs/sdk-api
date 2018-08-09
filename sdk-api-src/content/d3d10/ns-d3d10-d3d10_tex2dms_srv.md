---
UID: NS:d3d10.D3D10_TEX2DMS_SRV
title: D3D10_TEX2DMS_SRV
author: windows-sdk-content
description: Specifies the subresource(s) from a multisampled 2D texture to use in a shader-resource view.
old-location: direct3d10\d3d10_tex2dms_srv.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_tex2dms_srv.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 85d08460-6071-fabd-5910-b60baa79e1e6, D3D10_TEX2DMS_SRV, D3D10_TEX2DMS_SRV structure [Direct3D 10], d3d10/D3D10_TEX2DMS_SRV, direct3d10.d3d10_tex2dms_srv
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D10_TEX2DMS_SRV
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_TEX2DMS_SRV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_TEX2DMS_SRV structure


## -description


Specifies the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">subresource(s)</a> from a multisampled <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">2D texture</a> to use in a shader-resource view.


## -struct-fields




### -field UnusedField_NothingToDefine

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Integer of any value. See remarks.


## -remarks



Since a multisampled 2D texture contains a single subresource, there is actually nothing to specify in <a href="https://msdn.microsoft.com/en-us/library/Bb172468(v=VS.85).aspx">D3D10_TEX2DMS_RTV</a>. Consequently, <b>UnusedField_NothingToDefine</b> is included so that this structure will compile in C.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205277(v=VS.85).aspx">Resource Structures</a>
 

 

