---
UID: NF:strmif.IAMGraphStreams.SyncUsingStreamOffset
title: IAMGraphStreams::SyncUsingStreamOffset
author: windows-sdk-content
description: The SyncUsingStreamOffset method enables or disables synchronization using time-stamp offsets.
old-location: dshow\iamgraphstreams_syncusingstreamoffset.htm
old-project: DirectShow
ms.assetid: 1a61da3a-3933-4543-b733-1b8a60929e43
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IAMGraphStreams interface [DirectShow],SyncUsingStreamOffset method, IAMGraphStreams.SyncUsingStreamOffset, IAMGraphStreams::SyncUsingStreamOffset, IAMGraphStreamsSyncUsingStreamOffset, SyncUsingStreamOffset, SyncUsingStreamOffset method [DirectShow], SyncUsingStreamOffset method [DirectShow],IAMGraphStreams interface, dshow.iamgraphstreams_syncusingstreamoffset, strmif/IAMGraphStreams::SyncUsingStreamOffset
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
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
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMGraphStreams::SyncUsingStreamOffset


## -description



The <code>SyncUsingStreamOffset</code> method enables or disables synchronization using time-stamp offsets.




## -parameters




### -param bUseStreamOffset [in]

Boolean value indicating whether to use a time-stamp offset. If <b>TRUE</b>, live sources will use a time-stamp offset to synchronize streams.


## -returns



Returns S_OK if successsful, or an error code otherwise.




## -remarks



By default, the filter graph does not attempt to synchronize live streams by means of time-stamp offsets. Call this method with a value of <b>TRUE</b> if you want the filter graph to determine the maximum latency in the graph and adjust time stamps accordingly. For more information, see <a href="https://msdn.microsoft.com/a80d9f2e-6552-4bbb-9593-c1bef892548a">IAMPushSource::SetStreamOffset</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/30d44536-2a2d-44ab-bafc-bdb851cd272b">IAMGraphStreams Interface</a>
 

 

