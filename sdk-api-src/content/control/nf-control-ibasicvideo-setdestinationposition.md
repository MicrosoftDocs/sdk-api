---
UID: NF:control.IBasicVideo.SetDestinationPosition
title: IBasicVideo::SetDestinationPosition (control.h)
description: The SetDestinationPosition method sets the destination rectangle.
helpviewer_keywords: ["IBasicVideo interface [DirectShow]","SetDestinationPosition method","IBasicVideo.SetDestinationPosition","IBasicVideo::SetDestinationPosition","IBasicVideoSetDestinationPosition","SetDestinationPosition","SetDestinationPosition method [DirectShow]","SetDestinationPosition method [DirectShow]","IBasicVideo interface","control/IBasicVideo::SetDestinationPosition","dshow.ibasicvideo_setdestinationposition"]
old-location: dshow\ibasicvideo_setdestinationposition.htm
tech.root: dshow
ms.assetid: e638eb33-5a7f-4ebc-910f-72566e251f17
ms.date: 12/05/2018
ms.keywords: IBasicVideo interface [DirectShow],SetDestinationPosition method, IBasicVideo.SetDestinationPosition, IBasicVideo::SetDestinationPosition, IBasicVideoSetDestinationPosition, SetDestinationPosition, SetDestinationPosition method [DirectShow], SetDestinationPosition method [DirectShow],IBasicVideo interface, control/IBasicVideo::SetDestinationPosition, dshow.ibasicvideo_setdestinationposition
f1_keywords:
- control/IBasicVideo.SetDestinationPosition
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
- IBasicVideo.SetDestinationPosition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBasicVideo::SetDestinationPosition


## -description



The <code>SetDestinationPosition</code> method sets the destination rectangle.




## -parameters




### -param Left [in]

Specifies the x-coordinate, in pixels.


### -param Top [in]

Specifies the y-coordinate, in pixels.


### -param Width [in]

Specifies the width, in pixels.


### -param Height [in]

Specifies the height, in pixels.


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
Invalid argument. <i>Width</i> and <i>Height</i> must be larger than zero.

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
 




## -remarks



This method has the same effect as individually calling the <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-put_destinationleft">IBasicVideo::put_DestinationLeft</a>, <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-put_destinationtop">IBasicVideo::put_DestinationTop</a>, <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-put_destinationwidth">IBasicVideo::put_DestinationWidth</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ibasicvideo-put_destinationheight">IBasicVideo::put_DestinationHeight</a> methods.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo Interface</a>
 

 

