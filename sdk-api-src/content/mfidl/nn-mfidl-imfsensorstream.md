---
UID: NN:mfidl.IMFSensorStream
title: IMFSensorStream (mfidl.h)
description: .
helpviewer_keywords: ["IMFSensorStream","IMFSensorStream interface [Media Foundation]","IMFSensorStream interface [Media Foundation]","described","mf.imfsensorstream","mfidl/IMFSensorStream"]
old-location: mf\imfsensorstream.htm
tech.root: mf
ms.assetid: 9A5F6E25-796A-4798-8E4A-ABB9EB6A3B84
ms.date: 12/05/2018
ms.keywords: IMFSensorStream, IMFSensorStream interface [Media Foundation], IMFSensorStream interface [Media Foundation],described, mf.imfsensorstream, mfidl/IMFSensorStream
f1_keywords:
- mfidl/IMFSensorStream
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfplat.lib
- mfplat.dll
- mfplat.dll
- mfplat.dll.dll
api_name:
- IMFSensorStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSensorStream interface


## -description


Provides methods for cloning and querying the properties of a sensor stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSensorStream</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>. <b>IMFSensorStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSensorStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensorstream-clonesensorstream">CloneSensorStream</a>
</td>
<td align="left" width="63%">
Clones the <b>IMFSensorStream</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensorstream-getmediatype">GetMediaType</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> representing a supported media type for the sensor stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensorstream-getmediatypecount">GetMediaTypeCount</a>
</td>
<td align="left" width="63%">
Gets the count of media types supported by the sensor stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>
 

 

>>>>>>> master
