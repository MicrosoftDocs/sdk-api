---
UID: NF:strmif.IAMExtTransport.get_MediaState
title: IAMExtTransport::get_MediaState (strmif.h)
author: windows-sdk-content
description: The get_MediaState method retrieves the current state of the media.
old-location: dshow\iamexttransport_get_mediastate.htm
tech.root: DirectShow
ms.assetid: 806356c7-796e-459f-8d5f-82c6b744bf07
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMExtTransport interface [DirectShow],get_MediaState method, IAMExtTransport.get_MediaState, IAMExtTransport::get_MediaState, IAMExtTransportget_MediaState, dshow.iamexttransport_get_mediastate, get_MediaState, get_MediaState method [DirectShow], get_MediaState method [DirectShow],IAMExtTransport interface, strmif/IAMExtTransport::get_MediaState
ms.topic: method
req.header: strmif.h
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
 - IAMExtTransport.get_MediaState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMExtTransport::get_MediaState


## -description



The <code>get_MediaState</code> method retrieves the current state of the media.



This method is not implemented.


## -parameters




### -param pState [out]

Pointer to a <b>long</b> integer that receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_MEDIA_SPIN_DOWN</td>
<td>For disk media: Stopped spinning. For tape media: Tape is unthreaded.</td>
</tr>
<tr>
<td>ED_MEDIA_SPIN_UP</td>
<td>For disk media: Started spinning, but not at full speed. For tape media: Threading the tape.</td>
</tr>
<tr>
<td>ED_MEDIA_UNLOAD</td>
<td>Media is ejected from the drive.</td>
</tr>
</table>
 


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>
 

 

