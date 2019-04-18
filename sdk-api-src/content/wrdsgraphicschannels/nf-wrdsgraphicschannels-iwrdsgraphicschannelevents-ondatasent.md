---
UID: NF:wrdsgraphicschannels.IWRdsGraphicsChannelEvents.OnDataSent
title: IWRdsGraphicsChannelEvents::OnDataSent (wrdsgraphicschannels.h)
author: windows-sdk-content
description: Called when the IWRdsGraphicsChannel::Write method is called and the data has been sent.
old-location: termserv\iwrdsgraphicschannelevents_ondatasent.htm
tech.root: TermServ
ms.assetid: eb5af337-a412-4bda-862f-7e12705d0446
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWRdsGraphicsChannelEvents interface [Remote Desktop Services],OnDataSent method, IWRdsGraphicsChannelEvents.OnDataSent, IWRdsGraphicsChannelEvents::OnDataSent, OnDataSent, OnDataSent method [Remote Desktop Services], OnDataSent method [Remote Desktop Services],IWRdsGraphicsChannelEvents interface, termserv.iwrdsgraphicschannelevents_ondatasent, wrdsgraphicschannels/IWRdsGraphicsChannelEvents::OnDataSent
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
 - IWRdsGraphicsChannelEvents.OnDataSent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWRdsGraphicsChannelEvents::OnDataSent


## -description


Called when the <a href="https://msdn.microsoft.com/6ce627d8-078d-427a-b732-473d4f44f719">IWRdsGraphicsChannel::Write</a> method is called and the data has been sent. After this method has been called, the <i>pBuffer</i> parameter passed to the <a href="https://msdn.microsoft.com/6ce627d8-078d-427a-b732-473d4f44f719">IWRdsGraphicsChannel::Write</a> method is no longer needed and can be freed or reused.


## -parameters




### -param pWriteContext [in]

A user-defined interface pointer that is passed as the <i>pContext</i> parameter in the <a href="https://msdn.microsoft.com/6ce627d8-078d-427a-b732-473d4f44f719">IWRdsGraphicsChannel::Write</a> method.


### -param bCancelled [in]

Contains <b>TRUE</b> if the connection was dropped during the write, or <b>FALSE</b> otherwise.


### -param pBuffer [in]

A pointer to a buffer that contains the data that was sent. The <i>cbBuffer</i> parameter contains the length of this buffer.


### -param cbBuffer [in]

The length, in bytes, of the data in <i>pBuffer</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6ce627d8-078d-427a-b732-473d4f44f719">IWRdsGraphicsChannel::Write</a>



<a href="https://msdn.microsoft.com/59802a2d-bdb0-4792-b667-5095d4a02b06">IWRdsGraphicsChannelEvents</a>
 

 

