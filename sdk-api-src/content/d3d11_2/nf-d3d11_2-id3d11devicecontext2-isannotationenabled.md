---
UID: NF:d3d11_2.ID3D11DeviceContext2.IsAnnotationEnabled
title: ID3D11DeviceContext2::IsAnnotationEnabled
author: windows-driver-content
description: Allows apps to determine when either a capture or profiling request is enabled.
old-location: direct3d11\id3d11devicecontext2_isannotationenabled.htm
old-project: direct3d11
ms.assetid: 76096836-ab68-468e-a54a-a93ecb0bdb88
ms.author: windowsdriverdev
ms.date: 4/6/2018
ms.keywords: ID3D11DeviceContext2 interface [Direct3D 11],IsAnnotationEnabled method, ID3D11DeviceContext2.IsAnnotationEnabled, ID3D11DeviceContext2::IsAnnotationEnabled, IsAnnotationEnabled, IsAnnotationEnabled method [Direct3D 11], IsAnnotationEnabled method [Direct3D 11],ID3D11DeviceContext2 interface, d3d11_2/ID3D11DeviceContext2::IsAnnotationEnabled, direct3d11.id3d11devicecontext2_isannotationenabled
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: D3d11_2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_TILE_RANGE_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d11_2.h
api_name:
-	ID3D11DeviceContext2.IsAnnotationEnabled
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11DeviceContext2::IsAnnotationEnabled


## -description



   Allows apps to determine when either a capture or profiling request is enabled.


## -parameters






## -returns



Returns <b>TRUE</b> if capture or profiling is enabled and <b>FALSE</b> otherwise.




## -remarks



Returns <b>TRUE</b> if the capture tool is present and capturing or the app is being profiled such that <a href="https://msdn.microsoft.com/bb814f16-ca58-46ad-88eb-1c67b17d0c86">SetMarkerInt</a> or <a href="https://msdn.microsoft.com/9a45e16f-a598-4196-ad9c-8a157ae94de0">BeginEventInt</a> will be logged to <a href="ac99a063-e2d2-40cc-b659-d23c2f783f92">ETW</a>. Otherwise, it returns <b>FALSE</b>. Apps can use this to turn off self-throttling mechanisms in order to accurately capture what is currently being seen as app output. Apps can also avoid generating event markers and the associated overhead it may entail when there is no benefit to do so. 

If apps detect that capture is being performed, they can prevent the Direct3D debugging tools, such as Microsoft Visual Studio 2013, from capturing them. The purpose of the <a href="d3d11_create_device_flag.htm">D3D11_CREATE_DEVICE_PREVENT_ALTERING_LAYER_SETTINGS_FROM_REGISTRY</a> flag prior to Windows 8.1 was to allow the Direct3D runtime to prevent debugging tools from capturing apps.




## -see-also




<a href="https://msdn.microsoft.com/8B6B6F6E-9236-4DEE-A1BA-5FE45736DFAA">ID3D11DeviceContext2</a>
 

 

