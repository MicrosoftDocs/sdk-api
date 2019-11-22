---
UID: NF:wrdsgraphicschannels.IWRdsGraphicsChannel.Close
title: IWRdsGraphicsChannel::Close (wrdsgraphicschannels.h)

description: Called to close the channel.
old-location: termserv\iwrdsgraphicschannel_close.htm
tech.root: TermServ
ms.assetid: 6e3fb05d-0f5b-4ac3-b121-e6a1662c6ea2

ms.date: 12/05/2018
ms.keywords: Close, Close method [Remote Desktop Services], Close method [Remote Desktop Services],IWRdsGraphicsChannel interface, IWRdsGraphicsChannel interface [Remote Desktop Services],Close method, IWRdsGraphicsChannel.Close, IWRdsGraphicsChannel::Close, termserv.iwrdsgraphicschannel_close, wrdsgraphicschannels/IWRdsGraphicsChannel::Close
ms.topic: method
f1_keywords: 
 - "wrdsgraphicschannels/IWRdsGraphicsChannel.Close"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wrdsgraphicschannels.h
api_name:
 - IWRdsGraphicsChannel.Close
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWRdsGraphicsChannel::Close


## -description


Called to close the channel. The <a href="https://docs.microsoft.com/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannelevents-onclose">IWRdsGraphicsChannelEvents::OnClose</a> method will be called when the channel is completely closed.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wrdsgraphicschannels/nn-wrdsgraphicschannels-iwrdsgraphicschannel">IWRdsGraphicsChannel</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannelevents-onclose">IWRdsGraphicsChannelEvents::OnClose</a>
 

 

