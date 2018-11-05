---
UID: NF:dxgi1_2.IDXGIOutputDuplication.GetFrameMoveRects
title: IDXGIOutputDuplication::GetFrameMoveRects
author: windows-sdk-content
description: Gets information about the moved rectangles for the current desktop frame.
old-location: direct3ddxgi\idxgioutputduplication_getframemoverects.htm
tech.root: direct3ddxgi
ms.assetid: 7B7BF1A2-5F89-4AE1-BBDE-A298813B3AE7
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetFrameMoveRects, GetFrameMoveRects method [DXGI], GetFrameMoveRects method [DXGI],IDXGIOutputDuplication interface, IDXGIOutputDuplication interface [DXGI],GetFrameMoveRects method, IDXGIOutputDuplication.GetFrameMoveRects, IDXGIOutputDuplication::GetFrameMoveRects, direct3ddxgi.idxgioutputduplication_getframemoverects, dxgi1_2/IDXGIOutputDuplication::GetFrameMoveRects
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIOutputDuplication.GetFrameMoveRects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIOutputDuplication::GetFrameMoveRects


## -description


Gets information about the moved rectangles for the current desktop frame.


## -parameters




### -param MoveRectsBufferSize [in]

The size in bytes of the buffer that the caller passed to the  <i>pMoveRectBuffer</i> parameter.


### -param pMoveRectBuffer [out]

A pointer to an array of 
       <a href="https://msdn.microsoft.com/B19DB70A-83B4-4683-9E9B-3DA5D33AB564">DXGI_OUTDUPL_MOVE_RECT</a> structures 
       that identifies the moved rectangle regions for the desktop frame.


### -param pMoveRectsBufferSizeRequired [out]

Pointer to a variable that receives the number of bytes that 
       <b>GetFrameMoveRects</b> 
       needs to store information about moved regions in the buffer at <i>pMoveRectBuffer</i>.

For more information about returning the required buffer size, see Remarks.


## -returns



<b>GetFrameMoveRects</b> 
        returns:
        <ul>
<li>S_OK if it successfully retrieved information about moved rectangles.</li>
<li>DXGI_ERROR_ACCESS_LOST if the desktop duplication interface is invalid. The desktop duplication interface typically becomes invalid when a different type of image is displayed on the desktop.  Examples of this situation are: 
          <ul>
<li>Desktop switch</li>
<li>Mode change</li>
<li>Switch from DWM on, DWM off, or other full-screen application</li>
</ul>In this situation, the application must release the 
          <a href="https://msdn.microsoft.com/02C4EC3D-D97F-4CFC-ABF5-03B44CE6A658">IDXGIOutputDuplication</a> interface and 
          create a new <b>IDXGIOutputDuplication</b> 
          for the new content.</li>
<li>DXGI_ERROR_MORE_DATA if the buffer that the calling application provided 
          is not big enough.</li>
<li>DXGI_ERROR_INVALID_CALL if the application called 
          <b>GetFrameMoveRects</b> 
          without owning the desktop image.</li>
<li>E_INVALIDARG if one of the parameters to 
          <b>GetFrameMoveRects</b> 
          is incorrect; for example, if 
          <i>pMoveRectBuffer</i> is NULL.</li>
<li>Possibly other error codes that are described in the 
          <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.</li>
</ul>





## -remarks



<b>GetFrameMoveRects</b> 
      stores a size value in the variable at <i>pMoveRectsBufferSizeRequired</i>. This  value specifies the number of bytes that <b>GetFrameMoveRects</b> needs to store information about moved regions. You can use 
      this value in the following situations to determine the amount of memory to allocate for future buffers that you pass to <i>pMoveRectBuffer</i>:

<ul>
<li><b>GetFrameMoveRects</b> fails with DXGI_ERROR_MORE_DATA because the buffer is not big enough.</li>
<li><b>GetFrameMoveRects</b> supplies a buffer that is bigger than necessary. The size value returned at <i>pMoveRectsBufferSizeRequired</i> informs the caller how much buffer space was actually used compared to how much buffer space the caller allocated and specified in the  <i>MoveRectsBufferSize</i> parameter.</li>
</ul>
The caller can also use the value returned at <i>pMoveRectsBufferSizeRequired</i> to determine the number of <a href="https://msdn.microsoft.com/B19DB70A-83B4-4683-9E9B-3DA5D33AB564">DXGI_OUTDUPL_MOVE_RECT</a> structures returned.

The buffer contains the list of move RECTs for the current frame.

<div class="alert"><b>Note</b>  To produce a visually accurate copy of the desktop, an application must first process all move RECTs before it processes dirty RECTs.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/02C4EC3D-D97F-4CFC-ABF5-03B44CE6A658">IDXGIOutputDuplication</a>
 

 

