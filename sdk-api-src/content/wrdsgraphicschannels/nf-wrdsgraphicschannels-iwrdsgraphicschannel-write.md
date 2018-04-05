---
UID: NF:wrdsgraphicschannels.IWRdsGraphicsChannel.Write
title: IWRdsGraphicsChannel::Write method
author: windows-driver-content
description: Called to send data to the virtual channel.
old-location: termserv\iwrdsgraphicschannel_write.htm
old-project: TermServ
ms.assetid: 6ce627d8-078d-427a-b732-473d4f44f719
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IWRdsGraphicsChannel, IWRdsGraphicsChannel interface [Remote Desktop Services], Write method, IWRdsGraphicsChannel::Write, Write method [Remote Desktop Services], Write method [Remote Desktop Services], IWRdsGraphicsChannel interface, Write,IWRdsGraphicsChannel.Write, termserv.iwrdsgraphicschannel_write, wrdsgraphicschannels/IWRdsGraphicsChannel::Write
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
-	IWRdsGraphicsChannel.Write
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsGraphicsChannel::Write method


## -description


Called to send data to the virtual channel.


## -parameters




### -param cbSize [in]

The length, in bytes, of the data in <i>pBuffer</i>.


### -param pBuffer [in]

A pointer to a buffer that contains the data that was sent. The <i>cbBuffer</i> parameter contains the length of this buffer.

The implementation will take ownership of this buffer until the <a href="https://msdn.microsoft.com/eb5af337-a412-4bda-862f-7e12705d0446">IWRdsGraphicsChannelEvents::OnDataSent</a> method is called. Before that time, this buffer must not be modified or freed.


### -param pContext [in]

A user-defined interface pointer that is passed as the <i>pWriteContext</i> parameter in the <a href="https://msdn.microsoft.com/eb5af337-a412-4bda-862f-7e12705d0446">IWRdsGraphicsChannelEvents::OnDataSent</a> method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5d1e88b4-3dff-4f88-a6de-abc02da57ece">IWRdsGraphicsChannel</a>



<a href="https://msdn.microsoft.com/eb5af337-a412-4bda-862f-7e12705d0446">IWRdsGraphicsChannelEvents::OnDataSent</a>
 

 

