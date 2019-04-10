---
UID: NF:segment.IMSVidStreamBufferV2SourceEvent.ContentBecomingStale
title: IMSVidStreamBufferV2SourceEvent::ContentBecomingStale (segment.h)
author: windows-sdk-content
description: Fired when the SBE2 source filter receives a STREAMBUFFER_EC_CONTENT_BECOMING_STALE event, which indicates the stream buffer source lags behind the stream buffer sink by more than a preset number of files.For more information, see IStreamBufferConfigure::GetBackingFileCount.
old-location: mstv\imsvidstreambufferv2sourceevent_contentbecomingstale.htm
tech.root: mstv
ms.assetid: b9af548a-9796-4dc0-8b78-46e529a484ce
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ContentBecomingStale, ContentBecomingStale method [Microsoft TV Technologies], ContentBecomingStale method [Microsoft TV Technologies],IMSVidStreamBufferV2SourceEvent interface, IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies],ContentBecomingStale method, IMSVidStreamBufferV2SourceEvent.ContentBecomingStale, IMSVidStreamBufferV2SourceEvent::ContentBecomingStale, mstv.imsvidstreambufferv2sourceevent_contentbecomingstale, segment/IMSVidStreamBufferV2SourceEvent::ContentBecomingStale
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - segment.h
api_name:
 - IMSVidStreamBufferV2SourceEvent.ContentBecomingStale
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidStreamBufferV2SourceEvent::ContentBecomingStale


## -description


Fired when the SBE2 source filter receives a <b>STREAMBUFFER_EC_CONTENT_BECOMING_STALE</b> event, which indicates  the stream buffer source lags behind the stream buffer sink by more than a preset number of files.

For more information, see <a href="https://msdn.microsoft.com/5bf2a99a-ed6b-4ce6-9190-756393afcef0">IStreamBufferConfigure::GetBackingFileCount</a>.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd694694(v=VS.85).aspx">IMSVidStreamBufferV2SourceEvent</a>



<a href="https://msdn.microsoft.com/5bf2a99a-ed6b-4ce6-9190-756393afcef0">IStreamBufferConfigure::GetBackingFileCount</a>



<a href="https://msdn.microsoft.com/84364aa4-7306-40ee-9f4d-0683c47965b5">Stream Buffer Engine Event Codes</a>
 

 

