---
UID: NF:d3d10.ID3D10Asynchronous.Begin
title: ID3D10Asynchronous::Begin (d3d10.h)
description: Starts the collection of GPU data.
helpviewer_keywords: ["6afd45da-6dfb-8e93-0007-ccacda13bbb7","Begin","Begin method [Direct3D 10]","Begin method [Direct3D 10]","ID3D10Asynchronous interface","ID3D10Asynchronous interface [Direct3D 10]","Begin method","ID3D10Asynchronous.Begin","ID3D10Asynchronous::Begin","d3d10/ID3D10Asynchronous::Begin","direct3d10.id3d10asynchronous_begin"]
old-location: direct3d10\id3d10asynchronous_begin.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10asynchronous_begin.htm
ms.date: 12/05/2018
ms.keywords: 6afd45da-6dfb-8e93-0007-ccacda13bbb7, Begin, Begin method [Direct3D 10], Begin method [Direct3D 10],ID3D10Asynchronous interface, ID3D10Asynchronous interface [Direct3D 10],Begin method, ID3D10Asynchronous.Begin, ID3D10Asynchronous::Begin, d3d10/ID3D10Asynchronous::Begin, direct3d10.id3d10asynchronous_begin
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Asynchronous::Begin
 - d3d10/ID3D10Asynchronous::Begin
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
 - ID3D10Asynchronous.Begin
---

# ID3D10Asynchronous::Begin


## -description

Starts the collection of GPU data.



## -remarks

Calling Begin starts the asynchronous collection of GPU data. Calling <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-end">ID3D10Asynchronous::End</a> causes data collection to stop.  
  See <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10asynchronous">ID3D10Asynchronous Interface</a> for additional information.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10asynchronous">ID3D10Asynchronous Interface</a>
