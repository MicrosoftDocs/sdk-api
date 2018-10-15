---
UID: NN:mfidl.IMFMediaSourcePresentationProvider
title: IMFMediaSourcePresentationProvider
author: windows-sdk-content
description: Provides notifications to the sequencer source.
old-location: mf\imfmediasourcepresentationprovider.htm
tech.root: medfound
ms.assetid: b6b36324-a315-42a0-bdbf-8d2cec6cde3f
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IMFMediaSourcePresentationProvider, IMFMediaSourcePresentationProvider interface [Media Foundation], IMFMediaSourcePresentationProvider interface [Media Foundation],described, b6b36324-a315-42a0-bdbf-8d2cec6cde3f, mf.imfmediasourcepresentationprovider, mfidl/IMFMediaSourcePresentationProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IMFMediaSourcePresentationProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaSourcePresentationProvider interface


## -description


Provides notifications to the sequencer source. This interface is exposed by the sequencer source. Applications do not use this interface.

To get a pointer to this interface, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> with the service identifier MF_SOURCE_PRESENTATION_PROVIDER_SERVICE.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaSourcePresentationProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaSourcePresentationProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaSourcePresentationProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb2896f9-c397-4a0d-b8fe-b03ff4f08dda">ForceEndOfPresentation</a>
</td>
<td align="left" width="63%">
Notifies the source when playback has reached the end of a segment.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

