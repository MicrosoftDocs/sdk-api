---
UID: NS:dxgi1_2.DXGI_OUTDUPL_FRAME_INFO
title: DXGI_OUTDUPL_FRAME_INFO (dxgi1_2.h)
description: The DXGI_OUTDUPL_FRAME_INFO structure describes the current desktop image.
helpviewer_keywords: ["DXGI_OUTDUPL_FRAME_INFO","DXGI_OUTDUPL_FRAME_INFO structure [DXGI]","direct3ddxgi.dxgi_outdupl_frame_info","dxgi1_2/DXGI_OUTDUPL_FRAME_INFO"]
old-location: direct3ddxgi\dxgi_outdupl_frame_info.htm
tech.root: direct3ddxgi
ms.assetid: 2A5C6F99-0610-457D-9850-867DCDA8F293
ms.date: 12/05/2018
ms.keywords: DXGI_OUTDUPL_FRAME_INFO, DXGI_OUTDUPL_FRAME_INFO structure [DXGI], direct3ddxgi.dxgi_outdupl_frame_info, dxgi1_2/DXGI_OUTDUPL_FRAME_INFO
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
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
targetos: Windows
req.typenames: DXGI_OUTDUPL_FRAME_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_OUTDUPL_FRAME_INFO
 - dxgi1_2/DXGI_OUTDUPL_FRAME_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI1_2.h
api_name:
 - DXGI_OUTDUPL_FRAME_INFO
---

# DXGI_OUTDUPL_FRAME_INFO structure


## -description

The <b>DXGI_OUTDUPL_FRAME_INFO</b> structure describes the current desktop image.

## -struct-fields

### -field LastPresentTime

The time stamp of the last update of the desktop image.  The operating system calls the <a href="/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter">QueryPerformanceCounter</a> 
        function to obtain the value. A zero value indicates that the desktop image was not updated since an application last called the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe">IDXGIOutputDuplication::AcquireNextFrame</a> method to acquire the next frame of the desktop image.

### -field LastMouseUpdateTime

The time stamp of the last update to the mouse.  The operating system calls the <a href="/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter">QueryPerformanceCounter</a> 
        function to obtain the value. A zero value indicates that the position or shape of the mouse was not updated since an application last called the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe">IDXGIOutputDuplication::AcquireNextFrame</a> method to acquire the next frame of the desktop image.  The mouse position is always supplied for a mouse update. A new pointer shape is indicated by a non-zero value in the <b>PointerShapeBufferSize</b> member.

### -field AccumulatedFrames

The number of frames that the operating system accumulated in the desktop image surface since the calling application processed the last desktop image.  For more information about this number, see Remarks.

### -field RectsCoalesced

Specifies whether the operating system accumulated updates by coalescing dirty regions. Therefore,  the dirty regions might contain unmodified pixels. <b>TRUE</b> if dirty regions were accumulated; otherwise, <b>FALSE</b>.

### -field ProtectedContentMaskedOut

Specifies whether the desktop image might contain protected content that was already blacked out in the desktop image.  <b>TRUE</b> if protected content was already blacked; otherwise, <b>FALSE</b>. The application can use this information to notify the remote user that some of the desktop content might be protected and therefore not visible.

### -field PointerPosition

A <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_outdupl_pointer_position">DXGI_OUTDUPL_POINTER_POSITION</a> structure that describes the most recent mouse position if the <b>LastMouseUpdateTime</b> member is a non-zero value; otherwise, this value is ignored. This value provides the coordinates of the location where the top-left-hand corner of the pointer shape is drawn; this value is not the desktop position of the hot spot.

### -field TotalMetadataBufferSize

Size in bytes of the buffers to store all the desktop update metadata for this frame. For more information about this size, see Remarks.

### -field PointerShapeBufferSize

Size in bytes of the buffer to hold the new pixel data for the mouse shape. For more information about this size, see Remarks.

## -remarks

A non-zero <b>LastMouseUpdateTime</b> indicates an update to either a mouse pointer position or a mouse pointer position and shape. That is, the mouse pointer position is always valid for a non-zero <b>LastMouseUpdateTime</b>; however, the application must check the value of the <b>PointerShapeBufferSize</b> member to determine whether the shape was updated too.

If only the pointer was updated (that is, the desktop image was not updated), the <b>AccumulatedFrames</b>, <b>TotalMetadataBufferSize</b>, and <b>LastPresentTime</b> members are set to zero.

An <b>AccumulatedFrames</b> value of one indicates that the application completed processing the last frame before a new desktop image was presented.  If the <b>AccumulatedFrames</b> value is greater than one, more desktop image updates have occurred while the application processed the last desktop update. In this situation, the operating system accumulated the update regions. For more information about desktop updates, see Desktop Update Data.

A non-zero <b>TotalMetadataBufferSize</b> indicates the total size of the buffers that are required to store all the desktop update metadata.  An application cannot determine the size of each type of metadata.  The application must call the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects">IDXGIOutputDuplication::GetFrameDirtyRects</a>, <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects">IDXGIOutputDuplication::GetFrameMoveRects</a>, or <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape">IDXGIOutputDuplication::GetFramePointerShape</a> method to obtain information about each type of metadata.

<div class="alert"><b>Note</b>  To correct visual effects, an application must process the move region data before it processes the dirty rectangles.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>



<a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe">IDXGIOutputDuplication::AcquireNextFrame</a>