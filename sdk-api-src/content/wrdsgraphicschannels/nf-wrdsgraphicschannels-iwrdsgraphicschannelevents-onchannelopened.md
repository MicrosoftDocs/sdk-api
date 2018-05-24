---
UID: NF:wrdsgraphicschannels.IWRdsGraphicsChannelEvents.OnChannelOpened
title: IWRdsGraphicsChannelEvents::OnChannelOpened
author: windows-driver-content
description: Called when the channel has been opened and is ready for use, or when an error occurs when a channel is opened.
old-location: termserv\iwrdsgraphicschannelevents_onchannelopened.htm
old-project: TermServ
ms.assetid: dafff806-8b63-40cd-8b04-efb0497cb043
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IWRdsGraphicsChannelEvents interface [Remote Desktop Services],OnChannelOpened method, IWRdsGraphicsChannelEvents.OnChannelOpened, IWRdsGraphicsChannelEvents::OnChannelOpened, OnChannelOpened, OnChannelOpened method [Remote Desktop Services], OnChannelOpened method [Remote Desktop Services],IWRdsGraphicsChannelEvents interface, termserv.iwrdsgraphicschannelevents_onchannelopened, wrdsgraphicschannels/IWRdsGraphicsChannelEvents::OnChannelOpened
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
-	IWRdsGraphicsChannelEvents.OnChannelOpened
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsGraphicsChannelEvents::OnChannelOpened


## -description


Called when the channel has been opened and is ready for use, or when an error occurs when a channel is opened. The RemoteFX graphics services calls the <a href="https://msdn.microsoft.com/3b32b37f-6b1f-4682-9e2e-4a64e5c36e04">IWRdsGraphicsChannel::Open</a> method to open a channel. You must call the <b>OnChannelOpened</b> method to notify the RemoteFX graphics services that the channel is open and ready for use, or if an error occurs.


## -parameters




### -param OpenResult [in]

An <b>HRESULT</b> value that specifies the result of the open operation. If this parameter contains <b>S_OK</b>, <i>pOpenContext</i> is valid.


### -param pOpenContext [in]

A user-defined interface pointer that is passed as the <i>pOpenContext</i> parameter in the <a href="https://msdn.microsoft.com/3b32b37f-6b1f-4682-9e2e-4a64e5c36e04">IWRdsGraphicsChannel::Open</a> method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3b32b37f-6b1f-4682-9e2e-4a64e5c36e04">IWRdsGraphicsChannel::Open</a>



<a href="https://msdn.microsoft.com/59802a2d-bdb0-4792-b667-5095d4a02b06">IWRdsGraphicsChannelEvents</a>
 

 

