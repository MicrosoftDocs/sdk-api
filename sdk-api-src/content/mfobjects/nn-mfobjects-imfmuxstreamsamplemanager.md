---
UID: NN:mfobjects.IMFMuxStreamSampleManager
title: IMFMuxStreamSampleManager
author: windows-sdk-content
description: Provides the ability to retrieve IMFSample objects for individual substreams within the output of a multiplexed media source.
old-location: mf\imfmuxstreamsamplemanager.htm
old-project: medfound
ms.assetid: DABA5955-1366-4CEE-ABDF-7CC0F3788A8E
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IMFMuxStreamSampleManager, IMFMuxStreamSampleManager interface [Media Foundation], IMFMuxStreamSampleManager interface [Media Foundation],described, mf.imfmuxstreamsamplemanager, mfobjects/IMFMuxStreamSampleManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: MF_FILE_FLAGS
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
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFMuxStreamSampleManager interface


## -description


Provides the ability to retrieve <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> objects for individual substreams within the output of a multiplexed media source.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMuxStreamSampleManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMuxStreamSampleManager</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/F52147C3-FF6D-4F8F-93BE-2A3237C5A827">GetSample</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> associated with the substream with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4EC64809-4647-4AEE-98ED-2EB6CC0329DB">GetStreamConfiguration</a>
</td>
<td align="left" width="63%">
Gets the active stream configuration for the media source, which defines the set of substreams that are included  the  multiplexed output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7DB1AEAD-591F-4FA0-9DF0-9774C76A4B91">GetStreamCount</a>
</td>
<td align="left" width="63%">
Gets the count of substreams managed by the multiplexed media source.

</td>
</tr>
</table> 

