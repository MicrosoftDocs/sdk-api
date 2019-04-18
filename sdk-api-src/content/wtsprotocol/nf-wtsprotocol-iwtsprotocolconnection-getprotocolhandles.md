---
UID: NF:wtsprotocol.IWTSProtocolConnection.GetProtocolHandles
title: IWTSProtocolConnection::GetProtocolHandles (wtsprotocol.h)
author: windows-sdk-content
description: IWTSProtocolConnection::GetProtocolHandles is no longer available.
old-location: termserv\iwtsprotocolconnection_getprotocolhandles.htm
tech.root: TermServ
ms.assetid: d453ac71-4733-4a68-892c-ffca2d2954c6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetProtocolHandles, GetProtocolHandles method [Remote Desktop Services], GetProtocolHandles method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],GetProtocolHandles method, IWTSProtocolConnection.GetProtocolHandles, IWTSProtocolConnection::GetProtocolHandles, termserv.iwtsprotocolconnection_getprotocolhandles, wtsprotocol/IWTSProtocolConnection::GetProtocolHandles
ms.topic: method
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
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
 - Wtsprotocol.h
api_name:
 - IWTSProtocolConnection.GetProtocolHandles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSProtocolConnection::GetProtocolHandles


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::GetProtocolHandles</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/42f20dfc-e625-4b53-b055-750af4cbd3ec">IWRdsProtocolConnection::GetInputHandles</a> and <a href="https://msdn.microsoft.com/069ee899-ae3a-4043-92b5-e193dbfe4f54">IWRdsProtocolConnection::GetVideoHandle</a>.]

Retrieves keyboard, mouse, sound, and beep handles supported by the protocol.


## -parameters




### -param pKeyboardHandle [out]

A pointer to a keyboard handle. This is a handle to an <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff539967(v=vs.85).aspx">I8042prt keyboard driver</a>.


### -param pMouseHandle [out]

A pointer to a mouse handle. This is a handle to a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff542367(v=vs.85).aspx">Mouclass driver</a>.


### -param pBeepHandle [out]

A pointer to a beep device handle. This handle is not used and must be set to <b>NULL</b>.


### -param pVideoHandle [out]

 A pointer to a video device handle. This is a handle to the video miniport driver for the remote session associated with the protocol.


## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

