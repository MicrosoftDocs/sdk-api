---
UID: NF:d3d11_2.ID3D11DeviceContext2.IsAnnotationEnabled
title: ID3D11DeviceContext2::IsAnnotationEnabled (d3d11_2.h)
description: Allows apps to determine when either a capture or profiling request is enabled.
helpviewer_keywords: ["ID3D11DeviceContext2 interface [Direct3D 11]","IsAnnotationEnabled method","ID3D11DeviceContext2.IsAnnotationEnabled","ID3D11DeviceContext2::IsAnnotationEnabled","IsAnnotationEnabled","IsAnnotationEnabled method [Direct3D 11]","IsAnnotationEnabled method [Direct3D 11]","ID3D11DeviceContext2 interface","d3d11_2/ID3D11DeviceContext2::IsAnnotationEnabled","direct3d11.id3d11devicecontext2_isannotationenabled"]
old-location: direct3d11\id3d11devicecontext2_isannotationenabled.htm
tech.root: direct3d11
ms.assetid: 76096836-ab68-468e-a54a-a93ecb0bdb88
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext2 interface [Direct3D 11],IsAnnotationEnabled method, ID3D11DeviceContext2.IsAnnotationEnabled, ID3D11DeviceContext2::IsAnnotationEnabled, IsAnnotationEnabled, IsAnnotationEnabled method [Direct3D 11], IsAnnotationEnabled method [Direct3D 11],ID3D11DeviceContext2 interface, d3d11_2/ID3D11DeviceContext2::IsAnnotationEnabled, direct3d11.id3d11devicecontext2_isannotationenabled
req.header: d3d11_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: D3d11_2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext2::IsAnnotationEnabled
 - d3d11_2/ID3D11DeviceContext2::IsAnnotationEnabled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11_2.h
api_name:
 - ID3D11DeviceContext2.IsAnnotationEnabled
---

# ID3D11DeviceContext2::IsAnnotationEnabled


## -description

Allows apps to determine when either a capture or profiling request is enabled.



## -returns

Returns <b>TRUE</b> if capture or profiling is enabled and <b>FALSE</b> otherwise.

## -remarks

Returns <b>TRUE</b> if the capture tool is present and capturing or the app is being profiled such that <a href="/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-setmarkerint">SetMarkerInt</a> or <a href="/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-begineventint">BeginEventInt</a> will be logged to <a href="/previous-versions/dotnet/netframework-3.0/ms751538(v=vs.85)">ETW</a>. Otherwise, it returns <b>FALSE</b>. Apps can use this to turn off self-throttling mechanisms in order to accurately capture what is currently being seen as app output. Apps can also avoid generating event markers and the associated overhead it may entail when there is no benefit to do so. 

If apps detect that capture is being performed, they can prevent the Direct3D debugging tools, such as Microsoft Visual Studio 2013, from capturing them. The purpose of the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag">D3D11_CREATE_DEVICE_PREVENT_ALTERING_LAYER_SETTINGS_FROM_REGISTRY</a> flag prior to Windows 8.1 was to allow the Direct3D runtime to prevent debugging tools from capturing apps.

## -see-also

<a href="/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2">ID3D11DeviceContext2</a>
