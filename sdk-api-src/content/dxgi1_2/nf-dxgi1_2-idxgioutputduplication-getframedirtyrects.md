---
UID: NF:dxgi1_2.IDXGIOutputDuplication.GetFrameDirtyRects
title: IDXGIOutputDuplication::GetFrameDirtyRects (dxgi1_2.h)
description: Gets information about dirty rectangles for the current desktop frame.
helpviewer_keywords: ["GetFrameDirtyRects","GetFrameDirtyRects method [DXGI]","GetFrameDirtyRects method [DXGI]","IDXGIOutputDuplication interface","IDXGIOutputDuplication interface [DXGI]","GetFrameDirtyRects method","IDXGIOutputDuplication.GetFrameDirtyRects","IDXGIOutputDuplication::GetFrameDirtyRects","direct3ddxgi.idxgioutputduplication_getframedirtyrects","dxgi1_2/IDXGIOutputDuplication::GetFrameDirtyRects"]
old-location: direct3ddxgi\idxgioutputduplication_getframedirtyrects.htm
tech.root: direct3ddxgi
ms.assetid: F242E7C8-6A39-4B39-A811-243E17408577
ms.date: 12/05/2018
ms.keywords: GetFrameDirtyRects, GetFrameDirtyRects method [DXGI], GetFrameDirtyRects method [DXGI],IDXGIOutputDuplication interface, IDXGIOutputDuplication interface [DXGI],GetFrameDirtyRects method, IDXGIOutputDuplication.GetFrameDirtyRects, IDXGIOutputDuplication::GetFrameDirtyRects, direct3ddxgi.idxgioutputduplication_getframedirtyrects, dxgi1_2/IDXGIOutputDuplication::GetFrameDirtyRects
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
 - IDXGIOutputDuplication::GetFrameDirtyRects
 - dxgi1_2/IDXGIOutputDuplication::GetFrameDirtyRects
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
 - IDXGIOutputDuplication.GetFrameDirtyRects
---

# IDXGIOutputDuplication::GetFrameDirtyRects


## -description

Gets information about dirty rectangles for the current desktop frame.

## -parameters

### -param DirtyRectsBufferSize [in]

The size in bytes of the buffer that the caller passed to the  <i>pDirtyRectsBuffer</i> 
       parameter.

### -param pDirtyRectsBuffer [out]

A pointer to an array of <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structures 
        that identifies the dirty rectangle regions for the desktop frame.

### -param pDirtyRectsBufferSizeRequired [out]

Pointer to a variable that receives the number of bytes that 
       <b>GetFrameDirtyRects</b> 
       needs to store information about dirty regions in the buffer at 
       <i>pDirtyRectsBuffer</i>.

For more information about returning the required buffer size, see Remarks.

## -returns

<b>GetFrameDirtyRects</b> 
        returns:
        <ul>
<li>S_OK if it successfully retrieved information about dirty rectangles.</li>
<li>DXGI_ERROR_ACCESS_LOST if the desktop duplication interface is invalid. The desktop duplication 
          interface typically becomes invalid when a different type of image is displayed on the desktop. Examples of 
          this situation are: 
          <ul>
<li>Desktop switch</li>
<li>Mode change</li>
<li>Switch from DWM on, DWM off, or other full-screen application</li>
</ul>In this situation, the application must release the 
          <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutputduplication">IDXGIOutputDuplication</a> interface and 
          create a new 
          <b>IDXGIOutputDuplication</b> for the new 
          content.</li>
<li>DXGI_ERROR_MORE_DATA if the buffer that the calling application provided was not big enough.</li>
<li>DXGI_ERROR_INVALID_CALL if the application called 
          <b>GetFrameDirtyRects</b> 
          without owning the desktop image.</li>
<li>E_INVALIDARG if one of the parameters to 
          <b>GetFrameDirtyRects</b> 
          is incorrect; for example, if <i>pDirtyRectsBuffer</i> is NULL.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.</li>
</ul>

## -remarks

<b>GetFrameDirtyRects</b> stores a size value in the variable at <i>pDirtyRectsBufferSizeRequired</i>. This  value specifies the number of bytes that <b>GetFrameDirtyRects</b> needs to store information about dirty regions. You can use this value 
       in the following situations to determine the amount of memory to allocate for future buffers that you pass to <i>pDirtyRectsBuffer</i>:

<ul>
<li><b>GetFrameDirtyRects</b> 
      fails with DXGI_ERROR_MORE_DATA because the buffer is not big enough.</li>
<li><b>GetFrameDirtyRects</b> 
      supplies a buffer that is bigger than necessary. The size value returned at 
      <i>pDirtyRectsBufferSizeRequired</i> informs the caller how much buffer space was actually 
      used compared to how much buffer space the caller allocated and specified in the 
      <i>DirtyRectsBufferSize</i> parameter.</li>
</ul>
The caller can also use the value returned at <i>pDirtyRectsBufferSizeRequired</i> to 
     determine the number of <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>s returned in the <i>pDirtyRectsBuffer</i> array.

The buffer contains the list of dirty <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>s for the current frame.

<div class="alert"><b>Note</b>  To produce a visually accurate copy of the desktop, an application must first process all move <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>s before 
     it processes dirty <b>RECT</b>s.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutputduplication">IDXGIOutputDuplication</a>