---
UID: NN:mfreadwrite.IMFSourceReaderCallback2
title: IMFSourceReaderCallback2 (mfreadwrite.h)
author: windows-sdk-content
description: Extends the IMFSourceReaderCallback interface.
old-location: mf\imfsourcereadercallback2.htm
tech.root: medfound
ms.assetid: D0EC7FE9-74C3-4A7C-A5F3-798A3D6EF2CC
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFSourceReaderCallback2, IMFSourceReaderCallback2 interface [Media Foundation], IMFSourceReaderCallback2 interface [Media Foundation],described, mf.imfsourcereadercallback2, mfreadwrite/IMFSourceReaderCallback2
ms.topic: interface
f1_keywords: 
 - "mfreadwrite/IMFSourceReaderCallback2"
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - mfreadwrite.h
api_name:
 - IMFSourceReaderCallback2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSourceReaderCallback2 interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback">IMFSourceReaderCallback</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSourceReaderCallback2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSourceReaderCallback2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSourceReaderCallback2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback2-onstreamerror">OnStreamError</a>
</td>
<td align="left" width="63%">
Called when an asynchronous error occurs with the <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback2-ontransformchange">OnTransformChange</a>
</td>
<td align="left" width="63%">
Called when the transform chain in the <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a> is built or modified.

</td>
</tr>
</table> 


## -remarks



This interface provides a mechanism for apps that use <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a> to receive asynchronous notifications when the transform chain is complete and the system is ready for use or when an asynchronous error occurs.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

