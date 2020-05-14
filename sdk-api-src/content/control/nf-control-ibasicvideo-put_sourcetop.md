---
UID: NF:control.IBasicVideo.put_SourceTop
title: IBasicVideo::put_SourceTop (control.h)
description: The put_SourceTop method sets the y-coordinate of the source rectangle.helpviewer_keywords: ["IBasicVideo interface [DirectShow]","put_SourceTop method","IBasicVideo.put_SourceTop","IBasicVideo::put_SourceTop","IBasicVideoput_SourceTop","control/IBasicVideo::put_SourceTop","dshow.ibasicvideo_put_sourcetop","put_SourceTop","put_SourceTop method [DirectShow]","put_SourceTop method [DirectShow]","IBasicVideo interface"]
old-location: dshow\ibasicvideo_put_sourcetop.htm
tech.root: DirectShow
ms.assetid: 0a76518d-f79d-45ef-8e19-a3e5ee1e4db0
ms.date: 12/05/2018
ms.keywords: IBasicVideo interface [DirectShow],put_SourceTop method, IBasicVideo.put_SourceTop, IBasicVideo::put_SourceTop, IBasicVideoput_SourceTop, control/IBasicVideo::put_SourceTop, dshow.ibasicvideo_put_sourcetop, put_SourceTop, put_SourceTop method [DirectShow], put_SourceTop method [DirectShow],IBasicVideo interface
f1_keywords:
- control/IBasicVideo.put_SourceTop
dev_langs:
- c++
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
- IBasicVideo.put_SourceTop
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBasicVideo::put_SourceTop


## -description



The <code>put_SourceTop</code> method sets the y-coordinate of the source rectangle.




## -parameters




### -param SourceTop [in]

Specifies the y-coordinate, in pixels.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The video renderer's input pin is not connected.

</td>
</tr>
</table>
 




## -remarks



This method moves the entire source rectangle up or down. It does not change the height of the source rectangle. If the value of <i>SourceTop</i> would place the bottom edge of the rectangle beyond the edge of the video frame, the method returns E_INVALIDARG. To crop the video, call <b>put_SourceHeight</b> to adjust the width, before calling <code>put_SourceTop</code>. (Or call <b>SetSourcePosition</b> to set the entire source rectangle at once.)




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo Interface</a>
 

 

