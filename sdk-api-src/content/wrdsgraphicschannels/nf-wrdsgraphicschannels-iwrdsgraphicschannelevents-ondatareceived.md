---
UID: NF:wrdsgraphicschannels.IWRdsGraphicsChannelEvents.OnDataReceived
title: IWRdsGraphicsChannelEvents::OnDataReceived (wrdsgraphicschannels.h)
description: Called when a full message is received from the server.
helpviewer_keywords: ["IWRdsGraphicsChannelEvents interface [Remote Desktop Services]","OnDataReceived method","IWRdsGraphicsChannelEvents.OnDataReceived","IWRdsGraphicsChannelEvents::OnDataReceived","OnDataReceived","OnDataReceived method [Remote Desktop Services]","OnDataReceived method [Remote Desktop Services]","IWRdsGraphicsChannelEvents interface","termserv.iwrdsgraphicschannelevents_ondatareceived","wrdsgraphicschannels/IWRdsGraphicsChannelEvents::OnDataReceived"]
old-location: termserv\iwrdsgraphicschannelevents_ondatareceived.htm
tech.root: TermServ
ms.assetid: ac202fa0-6277-440a-8292-a785bbc78730
ms.date: 12/05/2018
ms.keywords: IWRdsGraphicsChannelEvents interface [Remote Desktop Services],OnDataReceived method, IWRdsGraphicsChannelEvents.OnDataReceived, IWRdsGraphicsChannelEvents::OnDataReceived, OnDataReceived, OnDataReceived method [Remote Desktop Services], OnDataReceived method [Remote Desktop Services],IWRdsGraphicsChannelEvents interface, termserv.iwrdsgraphicschannelevents_ondatareceived, wrdsgraphicschannels/IWRdsGraphicsChannelEvents::OnDataReceived
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
 - IWRdsGraphicsChannelEvents::OnDataReceived
 - wrdsgraphicschannels/IWRdsGraphicsChannelEvents::OnDataReceived
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
 - IWRdsGraphicsChannelEvents.OnDataReceived
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wrdsgraphicschannels/nn-wrdsgraphicschannels-iwrdsgraphicschannelevents">IWRdsGraphicsChannelEvents</a>