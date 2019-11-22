---
UID: NF:strmif.IVMRWindowlessControl.RepaintVideo
title: IVMRWindowlessControl::RepaintVideo (strmif.h)

description: The RepaintVideo method repaints the current video frame.
old-location: dshow\ivmrwindowlesscontrol_repaintvideo.htm
tech.root: DirectShow
ms.assetid: 16ef3bc1-1781-44f7-a997-ae9b1b3c405c

ms.date: 12/05/2018
ms.keywords: IVMRWindowlessControl interface [DirectShow],RepaintVideo method, IVMRWindowlessControl.RepaintVideo, IVMRWindowlessControl::RepaintVideo, IVMRWindowlessControlRepaintVideo, RepaintVideo, RepaintVideo method [DirectShow], RepaintVideo method [DirectShow],IVMRWindowlessControl interface, dshow.ivmrwindowlesscontrol_repaintvideo, strmif/IVMRWindowlessControl::RepaintVideo
ms.topic: method
f1_keywords: 
 - "strmif/IVMRWindowlessControl.RepaintVideo"
dev_langs:
 - c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IVMRWindowlessControl.RepaintVideo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRWindowlessControl::RepaintVideo


## -description



The <code>RepaintVideo</code> method repaints the current video frame.




## -parameters




### -param hwnd [in]

Specifies the handle of the window in which the repainting should occur.


### -param hdc [in]

Specifies the handle to the device context for the window.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrwindowlesscontrol">IVMRWindowlessControl Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

