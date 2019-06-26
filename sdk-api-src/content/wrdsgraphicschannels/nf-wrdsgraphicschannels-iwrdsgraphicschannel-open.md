---
UID: NF:wrdsgraphicschannels.IWRdsGraphicsChannel.Open
title: IWRdsGraphicsChannel::Open (wrdsgraphicschannels.h)
author: windows-sdk-content
description: Called to open a channel.
old-location: termserv\iwrdsgraphicschannel_open.htm
tech.root: TermServ
ms.assetid: 3b32b37f-6b1f-4682-9e2e-4a64e5c36e04
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWRdsGraphicsChannel interface [Remote Desktop Services],Open method, IWRdsGraphicsChannel.Open, IWRdsGraphicsChannel::Open, Open, Open method [Remote Desktop Services], Open method [Remote Desktop Services],IWRdsGraphicsChannel interface, termserv.iwrdsgraphicschannel_open, wrdsgraphicschannels/IWRdsGraphicsChannel::Open
ms.topic: method
f1_keywords: 
 - "wrdsgraphicschannels/IWRdsGraphicsChannel.Open"
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
 - IWRdsGraphicsChannel.Open
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWRdsGraphicsChannel::Open


## -description


Called to open a channel. When the channel is completely open and ready for use, you must call the <a href="https://docs.microsoft.com/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannelevents-onchannelopened">IWRdsGraphicsChannelEvents::OnChannelOpened</a> method.


## -parameters




### -param pChannelEvents [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wrdsgraphicschannels/nn-wrdsgraphicschannels-iwrdsgraphicschannelevents">IWRdsGraphicsChannelEvents</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wrdsgraphicschannels/nn-wrdsgraphicschannels-iwrdsgraphicschannelevents">IWRdsGraphicsChannelEvents</a> interface that will receive notifications relating to the channel created.


### -param pOpenContext [in]

Type: <b>IUnknown*</b>

A user-defined interface pointer that is passed as the <i>pOpenContext</i> parameter in the <a href="https://docs.microsoft.com/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannelevents-onchannelopened">IWRdsGraphicsChannelEvents::OnChannelOpened</a> method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wrdsgraphicschannels/nn-wrdsgraphicschannels-iwrdsgraphicschannel">IWRdsGraphicsChannel</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannelevents-onchannelopened">IWRdsGraphicsChannelEvents::OnChannelOpened</a>
 

 

