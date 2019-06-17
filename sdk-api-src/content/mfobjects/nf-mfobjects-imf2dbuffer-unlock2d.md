---
UID: NF:mfobjects.IMF2DBuffer.Unlock2D
title: IMF2DBuffer::Unlock2D (mfobjects.h)
author: windows-sdk-content
description: Unlocks a buffer that was previously locked. Call this method once for each call to IMF2DBuffer::Lock2D.
old-location: mf\imf2dbuffer_unlock2d.htm
tech.root: medfound
ms.assetid: 535452a3-0b38-467e-b556-80a069e4c0a5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 535452a3-0b38-467e-b556-80a069e4c0a5, IMF2DBuffer interface [Media Foundation],Unlock2D method, IMF2DBuffer.Unlock2D, IMF2DBuffer::Unlock2D, Unlock2D, Unlock2D method [Media Foundation], Unlock2D method [Media Foundation],IMF2DBuffer interface, mf.imf2dbuffer_unlock2d, mfobjects/IMF2DBuffer::Unlock2D
ms.topic: method
f1_keywords: ["mfobjects/IMF2DBuffer.Unlock2D"]
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMF2DBuffer.Unlock2D
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMF2DBuffer::Unlock2D


## -description



Unlocks a buffer that was previously locked. Call this method once for each call to <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d">IMF2DBuffer::Lock2D</a>.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-buffers">Media Buffers</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/uncompressed-video-buffers">Uncompressed Video Buffers</a>
 

 

