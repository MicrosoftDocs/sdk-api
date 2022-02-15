---
UID: NF:d3d11_2.ID3D11DeviceContext2.EndEvent
title: ID3D11DeviceContext2::EndEvent (d3d11_2.h)
description: Allows applications to annotate the end of a range of graphics commands.
helpviewer_keywords: ["EndEvent","EndEvent method [Direct3D 11]","EndEvent method [Direct3D 11]","ID3D11DeviceContext2 interface","ID3D11DeviceContext2 interface [Direct3D 11]","EndEvent method","ID3D11DeviceContext2.EndEvent","ID3D11DeviceContext2::EndEvent","d3d11_2/ID3D11DeviceContext2::EndEvent","direct3d11.id3d11devicecontext2_endevent"]
old-location: direct3d11\id3d11devicecontext2_endevent.htm
tech.root: direct3d11
ms.assetid: 1684ee4b-637d-4764-bb69-6ebc5c2985f1
ms.date: 12/05/2018
ms.keywords: EndEvent, EndEvent method [Direct3D 11], EndEvent method [Direct3D 11],ID3D11DeviceContext2 interface, ID3D11DeviceContext2 interface [Direct3D 11],EndEvent method, ID3D11DeviceContext2.EndEvent, ID3D11DeviceContext2::EndEvent, d3d11_2/ID3D11DeviceContext2::EndEvent, direct3d11.id3d11devicecontext2_endevent
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
 - ID3D11DeviceContext2::EndEvent
 - d3d11_2/ID3D11DeviceContext2::EndEvent
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
 - ID3D11DeviceContext2.EndEvent
---

# ID3D11DeviceContext2::EndEvent


## -description

Allows applications to annotate the end of a range of graphics commands.



## -remarks

<b>EndEvent</b> allows applications to annotate the end of a range of graphics commands, in order to provide more context to what the GPU is executing. When the appropriate <a href="/previous-versions/dotnet/netframework-3.0/ms751538(v=vs.85)">ETW</a> logging is not enabled, this method does nothing. When ETW logging is enabled, an additional marker is correlated between the CPU and GPU timelines.

## -see-also

<a href="/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2">ID3D11DeviceContext2</a>
