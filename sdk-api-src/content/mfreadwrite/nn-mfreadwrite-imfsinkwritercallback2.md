---
UID: NN:mfreadwrite.IMFSinkWriterCallback2
title: IMFSinkWriterCallback2 (mfreadwrite.h)
description: Extends the IMFSinkWriterCallback interface.
old-location: mf\imfsinkwritercallback2.htm
tech.root: medfound
ms.assetid: 92885A3C-137D-42DD-A65D-D2CE56A69A68
ms.date: 12/05/2018
ms.keywords: IMFSinkWriterCallback2, IMFSinkWriterCallback2 interface [Media Foundation], IMFSinkWriterCallback2 interface [Media Foundation],described, mf.imfsinkwritercallback2, mfreadwrite/IMFSinkWriterCallback2
ms.topic: interface
f1_keywords:
- mfreadwrite/IMFSinkWriterCallback2
dev_langs:
- c++
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
- IMFSinkWriterCallback2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSinkWriterCallback2 interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback">IMFSinkWriterCallback</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSinkWriterCallback2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSinkWriterCallback2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSinkWriterCallback2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwritercallback2-onstreamerror">OnStreamError</a>
</td>
<td align="left" width="63%">
Called when an asynchronous error occurs with the <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwritercallback2-ontransformchange">OnTransformChange</a>
</td>
<td align="left" width="63%">
Called when the transform chain in the <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a> is built or modified.

</td>
</tr>
</table> 


## -remarks



This interface provides a mechanism for apps that use <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a> to receive asynchronous notifications when the transform chain is complete and the system is ready for use or when an asynchronous error occurs.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

