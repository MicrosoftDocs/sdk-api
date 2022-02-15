---
UID: NF:strmif.IAMGraphStreams.SyncUsingStreamOffset
title: IAMGraphStreams::SyncUsingStreamOffset (strmif.h)
description: The SyncUsingStreamOffset method enables or disables synchronization using time-stamp offsets.
helpviewer_keywords: ["IAMGraphStreams interface [DirectShow]","SyncUsingStreamOffset method","IAMGraphStreams.SyncUsingStreamOffset","IAMGraphStreams::SyncUsingStreamOffset","IAMGraphStreamsSyncUsingStreamOffset","SyncUsingStreamOffset","SyncUsingStreamOffset method [DirectShow]","SyncUsingStreamOffset method [DirectShow]","IAMGraphStreams interface","dshow.iamgraphstreams_syncusingstreamoffset","strmif/IAMGraphStreams::SyncUsingStreamOffset"]
old-location: dshow\iamgraphstreams_syncusingstreamoffset.htm
tech.root: dshow
ms.assetid: 1a61da3a-3933-4543-b733-1b8a60929e43
ms.date: 12/05/2018
ms.keywords: IAMGraphStreams interface [DirectShow],SyncUsingStreamOffset method, IAMGraphStreams.SyncUsingStreamOffset, IAMGraphStreams::SyncUsingStreamOffset, IAMGraphStreamsSyncUsingStreamOffset, SyncUsingStreamOffset, SyncUsingStreamOffset method [DirectShow], SyncUsingStreamOffset method [DirectShow],IAMGraphStreams interface, dshow.iamgraphstreams_syncusingstreamoffset, strmif/IAMGraphStreams::SyncUsingStreamOffset
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMGraphStreams::SyncUsingStreamOffset
 - strmif/IAMGraphStreams::SyncUsingStreamOffset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMGraphStreams.SyncUsingStreamOffset
---

# IAMGraphStreams::SyncUsingStreamOffset


## -description

The <code>SyncUsingStreamOffset</code> method enables or disables synchronization using time-stamp offsets.

## -parameters

### -param bUseStreamOffset [in]

Boolean value indicating whether to use a time-stamp offset. If <b>TRUE</b>, live sources will use a time-stamp offset to synchronize streams.

## -returns

Returns S_OK if successful, or an error code otherwise.

## -remarks

By default, the filter graph does not attempt to synchronize live streams by means of time-stamp offsets. Call this method with a value of <b>TRUE</b> if you want the filter graph to determine the maximum latency in the graph and adjust time stamps accordingly. For more information, see <a href="/windows/desktop/api/strmif/nf-strmif-iampushsource-setstreamoffset">IAMPushSource::SetStreamOffset</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamgraphstreams">IAMGraphStreams Interface</a>