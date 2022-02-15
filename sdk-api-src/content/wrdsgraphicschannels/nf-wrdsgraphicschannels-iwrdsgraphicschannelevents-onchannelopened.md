---
UID: NF:wrdsgraphicschannels.IWRdsGraphicsChannelEvents.OnChannelOpened
title: IWRdsGraphicsChannelEvents::OnChannelOpened (wrdsgraphicschannels.h)
description: Called when the channel has been opened and is ready for use, or when an error occurs when a channel is opened.
helpviewer_keywords: ["IWRdsGraphicsChannelEvents interface [Remote Desktop Services]","OnChannelOpened method","IWRdsGraphicsChannelEvents.OnChannelOpened","IWRdsGraphicsChannelEvents::OnChannelOpened","OnChannelOpened","OnChannelOpened method [Remote Desktop Services]","OnChannelOpened method [Remote Desktop Services]","IWRdsGraphicsChannelEvents interface","termserv.iwrdsgraphicschannelevents_onchannelopened","wrdsgraphicschannels/IWRdsGraphicsChannelEvents::OnChannelOpened"]
old-location: termserv\iwrdsgraphicschannelevents_onchannelopened.htm
tech.root: TermServ
ms.assetid: dafff806-8b63-40cd-8b04-efb0497cb043
ms.date: 12/05/2018
ms.keywords: IWRdsGraphicsChannelEvents interface [Remote Desktop Services],OnChannelOpened method, IWRdsGraphicsChannelEvents.OnChannelOpened, IWRdsGraphicsChannelEvents::OnChannelOpened, OnChannelOpened, OnChannelOpened method [Remote Desktop Services], OnChannelOpened method [Remote Desktop Services],IWRdsGraphicsChannelEvents interface, termserv.iwrdsgraphicschannelevents_onchannelopened, wrdsgraphicschannels/IWRdsGraphicsChannelEvents::OnChannelOpened
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
 - IWRdsGraphicsChannelEvents::OnChannelOpened
 - wrdsgraphicschannels/IWRdsGraphicsChannelEvents::OnChannelOpened
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
 - IWRdsGraphicsChannelEvents.OnChannelOpened
---

# IWRdsGraphicsChannelEvents::OnChannelOpened


## -description

Called when the channel has been opened and is ready for use, or when an error occurs when a channel is opened. The RemoteFX graphics services calls the <a href="/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannel-open">IWRdsGraphicsChannel::Open</a> method to open a channel. You must call the <b>OnChannelOpened</b> method to notify the RemoteFX graphics services that the channel is open and ready for use, or if an error occurs.

## -parameters

### -param OpenResult [in]

An <b>HRESULT</b> value that specifies the result of the open operation. If this parameter contains <b>S_OK</b>, <i>pOpenContext</i> is valid.

### -param pOpenContext [in]

A user-defined interface pointer that is passed as the <i>pOpenContext</i> parameter in the <a href="/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannel-open">IWRdsGraphicsChannel::Open</a> method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannel-open">IWRdsGraphicsChannel::Open</a>



<a href="/windows/desktop/api/wrdsgraphicschannels/nn-wrdsgraphicschannels-iwrdsgraphicschannelevents">IWRdsGraphicsChannelEvents</a>