---
UID: NF:vmr9.IVMRWindowlessControl9.RepaintVideo
title: IVMRWindowlessControl9::RepaintVideo (vmr9.h)
author: windows-sdk-content
description: The RepaintVideo method repaints the current video frame.
old-location: dshow\ivmrwindowlesscontrol9_repaintvideo.htm
tech.root: DirectShow
ms.assetid: 7a25301c-00e4-4f54-a34d-416a52daeaa7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVMRWindowlessControl9 interface [DirectShow],RepaintVideo method, IVMRWindowlessControl9.RepaintVideo, IVMRWindowlessControl9::RepaintVideo, IVMRWindowlessControl9RepaintVideo, RepaintVideo, RepaintVideo method [DirectShow], RepaintVideo method [DirectShow],IVMRWindowlessControl9 interface, dshow.ivmrwindowlesscontrol9_repaintvideo, vmr9/IVMRWindowlessControl9::RepaintVideo
ms.topic: method
f1_keywords: 
 - "vmr9/IVMRWindowlessControl9.RepaintVideo"
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRWindowlessControl9.RepaintVideo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRWindowlessControl9::RepaintVideo


## -description



The <code>RepaintVideo</code> method repaints the current video frame.




## -parameters




### -param hwnd [in]

Specifies the handle of the window in which the repainting should occur.


### -param hdc [in]

Specifies the handle to the device context for the window.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The VMR is not in windowless mode.

</td>
</tr>
</table>
 




## -remarks



Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nn-vmr9-ivmrwindowlesscontrol9">IVMRWindowlessControl9 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

