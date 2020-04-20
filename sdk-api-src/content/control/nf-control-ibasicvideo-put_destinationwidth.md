---
UID: NF:control.IBasicVideo.put_DestinationWidth
title: IBasicVideo::put_DestinationWidth (control.h)
description: The put_DestinationWidth method sets the width of the destination rectangle.helpviewer_keywords: ["IBasicVideo interface [DirectShow]","put_DestinationWidth method","IBasicVideo.put_DestinationWidth","IBasicVideo::put_DestinationWidth","IBasicVideoput_DestinationWidth","control/IBasicVideo::put_DestinationWidth","dshow.ibasicvideo_put_destinationwidth","put_DestinationWidth","put_DestinationWidth method [DirectShow]","put_DestinationWidth method [DirectShow]","IBasicVideo interface"]
old-location: dshow\ibasicvideo_put_destinationwidth.htm
tech.root: DirectShow
ms.assetid: 4ae22194-19ca-4a20-9b4f-d9f39e346606
ms.date: 12/05/2018
ms.keywords: IBasicVideo interface [DirectShow],put_DestinationWidth method, IBasicVideo.put_DestinationWidth, IBasicVideo::put_DestinationWidth, IBasicVideoput_DestinationWidth, control/IBasicVideo::put_DestinationWidth, dshow.ibasicvideo_put_destinationwidth, put_DestinationWidth, put_DestinationWidth method [DirectShow], put_DestinationWidth method [DirectShow],IBasicVideo interface
f1_keywords:
- control/IBasicVideo.put_DestinationWidth
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
- IBasicVideo.put_DestinationWidth
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBasicVideo::put_DestinationWidth


## -description



The <code>put_DestinationWidth</code> method sets the width of the destination rectangle.




## -parameters




### -param DestinationWidth [in]

Specifies the width, in pixels.


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
Invalid argument. <i>DestinationWidth</i> must be larger than zero.

</td>
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
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The video renderer is not connected.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo Interface</a>
 

 

