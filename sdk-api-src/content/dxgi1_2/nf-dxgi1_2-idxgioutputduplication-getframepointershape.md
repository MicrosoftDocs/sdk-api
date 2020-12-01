---
UID: NF:dxgi1_2.IDXGIOutputDuplication.GetFramePointerShape
title: IDXGIOutputDuplication::GetFramePointerShape (dxgi1_2.h)
description: Gets information about the new pointer shape for the current desktop frame.
helpviewer_keywords: ["GetFramePointerShape","GetFramePointerShape method [DXGI]","GetFramePointerShape method [DXGI]","IDXGIOutputDuplication interface","IDXGIOutputDuplication interface [DXGI]","GetFramePointerShape method","IDXGIOutputDuplication.GetFramePointerShape","IDXGIOutputDuplication::GetFramePointerShape","direct3ddxgi.idxgioutputduplication_getframepointershape","dxgi1_2/IDXGIOutputDuplication::GetFramePointerShape"]
old-location: direct3ddxgi\idxgioutputduplication_getframepointershape.htm
tech.root: direct3ddxgi
ms.assetid: 321FDB62-BF0E-402E-A00B-6F60B7F132AA
ms.date: 12/05/2018
ms.keywords: GetFramePointerShape, GetFramePointerShape method [DXGI], GetFramePointerShape method [DXGI],IDXGIOutputDuplication interface, IDXGIOutputDuplication interface [DXGI],GetFramePointerShape method, IDXGIOutputDuplication.GetFramePointerShape, IDXGIOutputDuplication::GetFramePointerShape, direct3ddxgi.idxgioutputduplication_getframepointershape, dxgi1_2/IDXGIOutputDuplication::GetFramePointerShape
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxgi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIOutputDuplication::GetFramePointerShape
 - dxgi1_2/IDXGIOutputDuplication::GetFramePointerShape
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIOutputDuplication.GetFramePointerShape
---

# IDXGIOutputDuplication::GetFramePointerShape


## -description

Gets information about the new pointer shape for the current desktop frame.

## -parameters

### -param PointerShapeBufferSize [in]

The size in bytes of the buffer that the caller passed to the  <i>pPointerShapeBuffer</i> parameter.

### -param pPointerShapeBuffer [out]

A pointer to a buffer to which <b>GetFramePointerShape</b> copies and returns pixel data for the new pointer shape.

### -param pPointerShapeBufferSizeRequired [out]

Pointer to a variable that receives the number of bytes that <b>GetFramePointerShape</b> needs to store the new pointer shape pixel data in the buffer at <i>pPointerShapeBuffer</i>.

For more information about returning the required buffer size, see Remarks.

### -param pPointerShapeInfo [out]

Pointer to a <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_outdupl_pointer_shape_info">DXGI_OUTDUPL_POINTER_SHAPE_INFO</a> structure that receives the pointer shape information.

## -returns

<b>GetFramePointerShape</b> returns:
        <ul>
<li>S_OK if it successfully retrieved information about the new pointer shape.</li>
<li>DXGI_ERROR_ACCESS_LOST if the desktop duplication interface is invalid. The desktop duplication interface typically becomes invalid when a different type of image is displayed on the desktop.  Examples of this situation are: <ul>
<li>Desktop switch</li>
<li>Mode change</li>
<li>Switch from DWM on, DWM off, or other full-screen application</li>
</ul>In this situation, the application must release the <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutputduplication">IDXGIOutputDuplication</a> interface and create a new <b>IDXGIOutputDuplication</b> for the new content.</li>
<li>DXGI_ERROR_MORE_DATA if the buffer that the calling application provided was not big enough.</li>
<li>DXGI_ERROR_INVALID_CALL if the application called <b>GetFramePointerShape</b> without owning the desktop image.</li>
<li>E_INVALIDARG if one of the parameters to <b>GetFramePointerShape</b> is incorrect; for example, if <i>pPointerShapeInfo</i> is NULL.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.</li>
</ul>

## -remarks

<b>GetFramePointerShape</b> 
      stores a size value in the variable at <i>pPointerShapeBufferSizeRequired</i>. This  value specifies the number of bytes that <i>pPointerShapeBufferSizeRequired</i> needs to store the new pointer shape pixel data. You can use the value in the following situations to determine the amount of memory to allocate for future buffers that you pass to <i>pPointerShapeBuffer</i>:

<ul>
<li><b>GetFramePointerShape</b> fails with DXGI_ERROR_MORE_DATA because the buffer is not big enough.</li>
<li><b>GetFramePointerShape</b> supplies a bigger than necessary buffer. The size value returned at <i>pPointerShapeBufferSizeRequired</i> informs the caller how much buffer space was actually used compared to how much buffer space the caller allocated and specified in the  <i>PointerShapeBufferSize</i> parameter.</li>
</ul>
The <i>pPointerShapeInfo</i> parameter describes the new pointer shape.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutputduplication">IDXGIOutputDuplication</a>