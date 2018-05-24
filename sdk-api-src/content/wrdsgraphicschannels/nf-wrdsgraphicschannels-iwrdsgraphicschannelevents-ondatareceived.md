---
UID: NF:wrdsgraphicschannels.IWRdsGraphicsChannelEvents.OnDataReceived
title: IWRdsGraphicsChannelEvents::OnDataReceived
author: windows-driver-content
description: Called when a full message is received from the server.
old-location: termserv\iwrdsgraphicschannelevents_ondatareceived.htm
old-project: TermServ
ms.assetid: ac202fa0-6277-440a-8292-a785bbc78730
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IWRdsGraphicsChannelEvents interface [Remote Desktop Services],OnDataReceived method, IWRdsGraphicsChannelEvents.OnDataReceived, IWRdsGraphicsChannelEvents::OnDataReceived, OnDataReceived, OnDataReceived method [Remote Desktop Services], OnDataReceived method [Remote Desktop Services],IWRdsGraphicsChannelEvents interface, termserv.iwrdsgraphicschannelevents_ondatareceived, wrdsgraphicschannels/IWRdsGraphicsChannelEvents::OnDataReceived
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
-	IWRdsGraphicsChannelEvents.OnDataReceived
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsGraphicsChannelEvents::OnDataReceived


## -description


Called when a full message is received from the server.


## -parameters




### -param cbSize [in]

The length, in bytes, of the data in <i>pBuffer</i>.


### -param pBuffer [in]

A pointer to a buffer that contains the data that was received. The <i>cbSize</i> parameter contains the length of this buffer.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/59802a2d-bdb0-4792-b667-5095d4a02b06">IWRdsGraphicsChannelEvents</a>
 

 

