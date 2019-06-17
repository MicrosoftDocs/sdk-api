---
UID: NN:mfreadwrite.IMFSinkWriterEx
title: IMFSinkWriterEx (mfreadwrite.h)
author: windows-sdk-content
description: Extends the IMFSinkWriter interface.
old-location: mf\imfsinkwriterex.htm
tech.root: medfound
ms.assetid: 77E6CB22-E3B5-4D5E-8876-48582F75AA5C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFSinkWriterEx, IMFSinkWriterEx interface [Media Foundation], IMFSinkWriterEx interface [Media Foundation],described, mf.imfsinkwriterex, mfreadwrite/IMFSinkWriterEx
ms.topic: interface
f1_keywords: ["mfreadwrite/IMFSinkWriterEx"]
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFSinkWriterEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSinkWriterEx interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a> interface.

The <a href="https://docs.microsoft.com/windows/desktop/medfound/sink-writer">Sink Writer</a> implements this interface in Windows 8. To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> on the Sink Writer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSinkWriterEx</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>. <b>IMFSinkWriterEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSinkWriterEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriterex-gettransformforstream">GetTransformForStream</a>
</td>
<td align="left" width="63%">
Gets a pointer to a Media Foundation transform (MFT) for a specified stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/sink-writer">Sink Writer</a>
 

 

