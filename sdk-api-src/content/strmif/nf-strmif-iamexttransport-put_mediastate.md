---
UID: NF:strmif.IAMExtTransport.put_MediaState
title: IAMExtTransport::put_MediaState
author: windows-sdk-content
description: The put_MediaState method sets the current state of the media.
old-location: dshow\iamexttransport_put_mediastate.htm
old-project: DirectShow
ms.assetid: e5a4638e-3246-44dd-a7f8-52d0da12fc9c
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IAMExtTransport interface [DirectShow],put_MediaState method, IAMExtTransport.put_MediaState, IAMExtTransport::put_MediaState, IAMExtTransportput_MediaState, dshow.iamexttransport_put_mediastate, put_MediaState, put_MediaState method [DirectShow], put_MediaState method [DirectShow],IAMExtTransport interface, strmif/IAMExtTransport::put_MediaState
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMExtTransport.put_MediaState
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMExtTransport::put_MediaState


## -description



The <code>put_MediaState</code> method sets the current state of the media.




## -parameters




### -param State [in]

Specifies the media state as a <b>long</b> integer. Use one of the following:

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>ED_MEDIA_SPIN_DOWN</td>
<td>For disk media: Stop spinning. For tape media: Unthread the tape.</td>
</tr>
<tr>
<td>ED_MEDIA_SPIN_UP</td>
<td>For disk media: Start spinning. For tape media: Thread the tape.</td>
</tr>
<tr>
<td>ED_MEDIA_UNLOAD</td>
<td>Eject the media from the drive.</td>
</tr>
</table>
 

These constants are for disk and tape media. Other devices might need to define new constants.


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport Interface</a>



<a href="https://msdn.microsoft.com/806356c7-796e-459f-8d5f-82c6b744bf07">IAMExtTransport::get_MediaState</a>
 

 

