---
UID: NF:wrdsgraphicschannels.IWRdsGraphicsChannelEvents.OnDataSent
title: IWRdsGraphicsChannelEvents::OnDataSent (wrdsgraphicschannels.h)
description: Called when the IWRdsGraphicsChannel::Write method is called and the data has been sent.
helpviewer_keywords: ["IWRdsGraphicsChannelEvents interface [Remote Desktop Services]","OnDataSent method","IWRdsGraphicsChannelEvents.OnDataSent","IWRdsGraphicsChannelEvents::OnDataSent","OnDataSent","OnDataSent method [Remote Desktop Services]","OnDataSent method [Remote Desktop Services]","IWRdsGraphicsChannelEvents interface","termserv.iwrdsgraphicschannelevents_ondatasent","wrdsgraphicschannels/IWRdsGraphicsChannelEvents::OnDataSent"]
old-location: termserv\iwrdsgraphicschannelevents_ondatasent.htm
tech.root: TermServ
ms.assetid: eb5af337-a412-4bda-862f-7e12705d0446
ms.date: 12/05/2018
ms.keywords: IWRdsGraphicsChannelEvents interface [Remote Desktop Services],OnDataSent method, IWRdsGraphicsChannelEvents.OnDataSent, IWRdsGraphicsChannelEvents::OnDataSent, OnDataSent, OnDataSent method [Remote Desktop Services], OnDataSent method [Remote Desktop Services],IWRdsGraphicsChannelEvents interface, termserv.iwrdsgraphicschannelevents_ondatasent, wrdsgraphicschannels/IWRdsGraphicsChannelEvents::OnDataSent
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
 - IWRdsGraphicsChannelEvents::OnDataSent
 - wrdsgraphicschannels/IWRdsGraphicsChannelEvents::OnDataSent
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
 - IWRdsGraphicsChannelEvents.OnDataSent
---

# IWRdsGraphicsChannelEvents::OnDataSent


## -description

Called when the <a href="/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannel-write">IWRdsGraphicsChannel::Write</a> method is called and the data has been sent. After this method has been called, the <i>pBuffer</i> parameter passed to the <a href="/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannel-write">IWRdsGraphicsChannel::Write</a> method is no longer needed and can be freed or reused.

## -parameters

### -param pWriteContext [in]

A user-defined interface pointer that is passed as the <i>pContext</i> parameter in the <a href="/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannel-write">IWRdsGraphicsChannel::Write</a> method.

### -param bCancelled [in]

Contains <b>TRUE</b> if the connection was dropped during the write, or <b>FALSE</b> otherwise.

### -param pBuffer [in]

A pointer to a buffer that contains the data that was sent. The <i>cbBuffer</i> parameter contains the length of this buffer.

### -param cbBuffer [in]

The length, in bytes, of the data in <i>pBuffer</i>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannel-write">IWRdsGraphicsChannel::Write</a>



<a href="/windows/desktop/api/wrdsgraphicschannels/nn-wrdsgraphicschannels-iwrdsgraphicschannelevents">IWRdsGraphicsChannelEvents</a>