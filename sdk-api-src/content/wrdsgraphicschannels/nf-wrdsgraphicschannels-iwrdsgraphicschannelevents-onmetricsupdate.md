---
UID: NF:wrdsgraphicschannels.IWRdsGraphicsChannelEvents.OnMetricsUpdate
title: IWRdsGraphicsChannelEvents::OnMetricsUpdate (wrdsgraphicschannels.h)
description: Called to notify the RemoteFX graphics services that network conditions have changed.
helpviewer_keywords: ["IWRdsGraphicsChannelEvents interface [Remote Desktop Services]","OnMetricsUpdate method","IWRdsGraphicsChannelEvents.OnMetricsUpdate","IWRdsGraphicsChannelEvents::OnMetricsUpdate","OnMetricsUpdate","OnMetricsUpdate method [Remote Desktop Services]","OnMetricsUpdate method [Remote Desktop Services]","IWRdsGraphicsChannelEvents interface","termserv.iwrdsgraphicschannelevents_onmetricsupdate","wrdsgraphicschannels/IWRdsGraphicsChannelEvents::OnMetricsUpdate"]
old-location: termserv\iwrdsgraphicschannelevents_onmetricsupdate.htm
tech.root: TermServ
ms.assetid: d955041a-6179-4bf2-9a1b-766f459f3776
ms.date: 12/05/2018
ms.keywords: IWRdsGraphicsChannelEvents interface [Remote Desktop Services],OnMetricsUpdate method, IWRdsGraphicsChannelEvents.OnMetricsUpdate, IWRdsGraphicsChannelEvents::OnMetricsUpdate, OnMetricsUpdate, OnMetricsUpdate method [Remote Desktop Services], OnMetricsUpdate method [Remote Desktop Services],IWRdsGraphicsChannelEvents interface, termserv.iwrdsgraphicschannelevents_onmetricsupdate, wrdsgraphicschannels/IWRdsGraphicsChannelEvents::OnMetricsUpdate
req.header: wrdsgraphicschannels.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wrdsgraphicschannels.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWRdsGraphicsChannelEvents::OnMetricsUpdate
 - wrdsgraphicschannels/IWRdsGraphicsChannelEvents::OnMetricsUpdate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wrdsgraphicschannels.h
api_name:
 - IWRdsGraphicsChannelEvents.OnMetricsUpdate
---

# IWRdsGraphicsChannelEvents::OnMetricsUpdate


## -description

Called to notify the RemoteFX graphics services that network conditions have changed.

## -parameters

### -param bandwidth [in]

The expected bandwidth, in bytes per second. If this parameter contains <b>WRdsGraphicsChannels_Bandwidth_Unavailable</b>, bandwidth statistics are not available.

### -param RTT [in]

The round trip time (RTT) of the link, in milliseconds. If this parameter contains <b>WRdsGraphicsChannels_RTT_Unavailable</b>, latency statistics are not available.

### -param lastSentByteIndex [in]

The byte index of the last byte that was sent from this channel at this time. This value begins at zero and increases for the lifetime of the connection. This value will roll back to zero when an overflow occurs.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wrdsgraphicschannels/nn-wrdsgraphicschannels-iwrdsgraphicschannelevents">IWRdsGraphicsChannelEvents</a>