---
UID: NN:d3d10sdklayers.ID3D10SwitchToRef
title: ID3D10SwitchToRef (d3d10sdklayers.h)
description: A switch-to-reference interface (see the switch-to-reference layer) enables an application to switch between a hardware and software device.
helpviewer_keywords: ["ID3D10SwitchToRef","ID3D10SwitchToRef interface [Direct3D 10]","ID3D10SwitchToRef interface [Direct3D 10]","described","d3d10sdklayers/ID3D10SwitchToRef","d7769c3f-e1b2-ded4-9352-be26f55a05d1","direct3d10.id3d10switchtoref"]
old-location: direct3d10\id3d10switchtoref.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10switchtoref.htm
ms.date: 12/05/2018
ms.keywords: ID3D10SwitchToRef, ID3D10SwitchToRef interface [Direct3D 10], ID3D10SwitchToRef interface [Direct3D 10],described, d3d10sdklayers/ID3D10SwitchToRef, d7769c3f-e1b2-ded4-9352-be26f55a05d1, direct3d10.id3d10switchtoref
req.header: d3d10sdklayers.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10SwitchToRef
 - d3d10sdklayers/ID3D10SwitchToRef
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10SwitchToRef
---

# ID3D10SwitchToRef interface


## -description

A switch-to-reference interface (see the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-api-features-layers">switch-to-reference</a> layer) enables an application to switch between a hardware and software device.

## -inheritance

The <b>ID3D10SwitchToRef</b> interface inherits from <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>. <b>ID3D10SwitchToRef</b> also has these types of members:

## -remarks

This interface is obtained by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on a <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a> created with the <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag">D3D10_CREATE_DEVICE_SWITCH_TO_REF</a> flag.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>
