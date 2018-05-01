---
UID: NF:wrdsgraphicschannels.IWRdsGraphicsChannel.Open
title: IWRdsGraphicsChannel::Open method
author: windows-driver-content
description: Called to open a channel.
old-location: termserv\iwrdsgraphicschannel_open.htm
old-project: TermServ
ms.assetid: 3b32b37f-6b1f-4682-9e2e-4a64e5c36e04
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: IWRdsGraphicsChannel, IWRdsGraphicsChannel interface [Remote Desktop Services], Open method, IWRdsGraphicsChannel::Open, Open method [Remote Desktop Services], Open method [Remote Desktop Services], IWRdsGraphicsChannel interface, Open,IWRdsGraphicsChannel.Open, termserv.iwrdsgraphicschannel_open, wrdsgraphicschannels/IWRdsGraphicsChannel::Open
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: WRdsGraphicsChannelType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wrdsgraphicschannels.h
api_name:
-	IWRdsGraphicsChannel.Open
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsGraphicsChannel::Open method


## -description



    Called to open a channel. When the channel is completely open and ready for use, you must call the <a href="https://msdn.microsoft.com/dafff806-8b63-40cd-8b04-efb0497cb043">IWRdsGraphicsChannelEvents::OnChannelOpened</a> method.


## -parameters




### -param pChannelEvents [in]

Type: <b><a href="https://msdn.microsoft.com/59802a2d-bdb0-4792-b667-5095d4a02b06">IWRdsGraphicsChannelEvents</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/59802a2d-bdb0-4792-b667-5095d4a02b06">IWRdsGraphicsChannelEvents</a> interface that will receive notifications relating to the channel created.


### -param pOpenContext [in]

Type: <b>IUnknown*</b>

A user-defined interface pointer that is passed as the <i>pOpenContext</i> parameter in the <a href="https://msdn.microsoft.com/dafff806-8b63-40cd-8b04-efb0497cb043">IWRdsGraphicsChannelEvents::OnChannelOpened</a> method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5d1e88b4-3dff-4f88-a6de-abc02da57ece">IWRdsGraphicsChannel</a>



<a href="https://msdn.microsoft.com/dafff806-8b63-40cd-8b04-efb0497cb043">IWRdsGraphicsChannelEvents::OnChannelOpened</a>
 

 

