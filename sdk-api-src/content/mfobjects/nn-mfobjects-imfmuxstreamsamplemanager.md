---
UID: NN:mfobjects.IMFMuxStreamSampleManager
title: IMFMuxStreamSampleManager (mfobjects.h)
author: windows-sdk-content
description: Provides the ability to retrieve IMFSample objects for individual substreams within the output of a multiplexed media source.
old-location: mf\imfmuxstreamsamplemanager.htm
tech.root: medfound
ms.assetid: DABA5955-1366-4CEE-ABDF-7CC0F3788A8E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFMuxStreamSampleManager, IMFMuxStreamSampleManager interface [Media Foundation], IMFMuxStreamSampleManager interface [Media Foundation],described, mf.imfmuxstreamsamplemanager, mfobjects/IMFMuxStreamSampleManager
ms.topic: interface
f1_keywords: 
 - "mfobjects/IMFMuxStreamSampleManager"
dev_langs:
 - c++
req.header: mfobjects.h
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
 - IMFMuxStreamSampleManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMuxStreamSampleManager interface


## -description


Provides the ability to retrieve <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> objects for individual substreams within the output of a multiplexed media source.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMuxStreamSampleManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMuxStreamSampleManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMuxStreamSampleManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmuxstreamsamplemanager-getsample">GetSample</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> associated with the substream with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmuxstreamsamplemanager-getstreamconfiguration">GetStreamConfiguration</a>
</td>
<td align="left" width="63%">
Gets the active stream configuration for the media source, which defines the set of substreams that are included  the  multiplexed output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmuxstreamsamplemanager-getstreamcount">GetStreamCount</a>
</td>
<td align="left" width="63%">
Gets the count of substreams managed by the multiplexed media source.

</td>
</tr>
</table> 

