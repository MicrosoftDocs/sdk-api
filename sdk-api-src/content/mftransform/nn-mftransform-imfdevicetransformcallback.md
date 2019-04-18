---
UID: NN:mftransform.IMFDeviceTransformCallback
title: IMFDeviceTransformCallback (mftransform.h)
author: windows-sdk-content
description: Implement this callback to receive notifications when system-allocated frame buffers are sent to the device driver.
old-location: stream\imfdevicetransformcallback.htm
tech.root: stream
ms.assetid: F603F92A-9233-4786-9DE8-AE10BA981DE3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFDeviceTransformCallback, IMFDeviceTransformCallback interface [Streaming Media Devices], IMFDeviceTransformCallback interface [Streaming Media Devices],described, mftransform/IMFDeviceTransformCallback, stream.imfdevicetransformcallback
ms.topic: interface
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mftransform.h
api_name:
 - IMFDeviceTransformCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFDeviceTransformCallback interface


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Implement this callback to receive notifications when system-allocated frame buffers are sent to the device driver.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFDeviceTransformCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFDeviceTransformCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFDeviceTransformCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8736BF02-636A-4894-AA74-92A805152D52">OnBufferSent</a>
</td>
<td align="left" width="63%">
Called when system-allocated frame buffers are sent to the device driver. 

</td>
</tr>
</table> 

