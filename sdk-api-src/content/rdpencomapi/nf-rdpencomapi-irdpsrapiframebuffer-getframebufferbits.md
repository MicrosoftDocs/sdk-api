---
UID: NF:rdpencomapi.IRDPSRAPIFrameBuffer.GetFrameBufferBits
title: IRDPSRAPIFrameBuffer::GetFrameBufferBits (rdpencomapi.h)
description: Gets the bits in a specified area of the frame.
helpviewer_keywords: ["GetFrameBufferBits","GetFrameBufferBits method [RDP]","GetFrameBufferBits method [RDP]","IRDPSRAPIFrameBuffer interface","IRDPSRAPIFrameBuffer interface [RDP]","GetFrameBufferBits method","IRDPSRAPIFrameBuffer.GetFrameBufferBits","IRDPSRAPIFrameBuffer::GetFrameBufferBits","rdp.irdpsrapiframebuffer_getframebufferbits","rdpencomapi/IRDPSRAPIFrameBuffer::GetFrameBufferBits"]
old-location: rdp\irdpsrapiframebuffer_getframebufferbits.htm
tech.root: rdp
ms.assetid: 6497d9d1-c987-40ea-b384-0fff1e852122
ms.date: 12/05/2018
ms.keywords: GetFrameBufferBits, GetFrameBufferBits method [RDP], GetFrameBufferBits method [RDP],IRDPSRAPIFrameBuffer interface, IRDPSRAPIFrameBuffer interface [RDP],GetFrameBufferBits method, IRDPSRAPIFrameBuffer.GetFrameBufferBits, IRDPSRAPIFrameBuffer::GetFrameBufferBits, rdp.irdpsrapiframebuffer_getframebufferbits, rdpencomapi/IRDPSRAPIFrameBuffer::GetFrameBufferBits
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRDPSRAPIFrameBuffer::GetFrameBufferBits
 - rdpencomapi/IRDPSRAPIFrameBuffer::GetFrameBufferBits
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIFrameBuffer.GetFrameBufferBits
---

# IRDPSRAPIFrameBuffer::GetFrameBufferBits


## -description

Gets the bits in a specified area of the frame.

## -parameters

### -param x [in]

The x coordinate of the requested area of the frame.

### -param y [in]

The y coordinate of the requested area of the frame.

### -param Width [in]

The width of the requested area of the frame.

### -param Height [in]

The height of the requested area of the frame.

### -param ppBits [out, retval]

The contents of the frame buffer in the specified area.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiframebuffer">IRDPSRAPIFrameBuffer</a>