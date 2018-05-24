---
UID: NS:d3d10.D3D10_TEX2DMS_SRV
title: D3D10_TEX2DMS_SRV
author: windows-driver-content
description: Specifies the subresource(s) from a multisampled 2D texture to use in a shader-resource view.
old-location: direct3d10\d3d10_tex2dms_srv.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_tex2dms_srv.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: 85d08460-6071-fabd-5910-b60baa79e1e6, D3D10_TEX2DMS_SRV, D3D10_TEX2DMS_SRV structure [Direct3D 10], d3d10/D3D10_TEX2DMS_SRV, direct3d10.d3d10_tex2dms_srv
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
req.typenames: D3D10_TEX2DMS_SRV
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D10.h
api_name:
-	D3D10_TEX2DMS_SRV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_TEX2DMS_SRV structure


## -description


Specifies the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">subresource(s)</a> from a multisampled <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">2D texture</a> to use in a shader-resource view.


## -struct-fields




### -field UnusedField_NothingToDefine

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Integer of any value. See remarks.


## -remarks



Since a multisampled 2D texture contains a single subresource, there is actually nothing to specify in <a href="https://msdn.microsoft.com/458b8bed-42c3-45c5-96c7-fd7cb3964f6d">D3D10_TEX2DMS_RTV</a>. Consequently, <b>UnusedField_NothingToDefine</b> is included so that this structure will compile in C.




## -see-also




<a href="https://msdn.microsoft.com/d8fe2ebe-349a-456e-9a5a-16f2d3419800">Resource Structures</a>
 

 

