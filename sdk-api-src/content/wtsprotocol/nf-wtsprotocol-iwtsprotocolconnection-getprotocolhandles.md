---
UID: NF:wtsprotocol.IWTSProtocolConnection.GetProtocolHandles
title: IWTSProtocolConnection::GetProtocolHandles (wtsprotocol.h)
description: IWTSProtocolConnection::GetProtocolHandles is no longer available.
helpviewer_keywords: ["GetProtocolHandles","GetProtocolHandles method [Remote Desktop Services]","GetProtocolHandles method [Remote Desktop Services]","IWTSProtocolConnection interface","IWTSProtocolConnection interface [Remote Desktop Services]","GetProtocolHandles method","IWTSProtocolConnection.GetProtocolHandles","IWTSProtocolConnection::GetProtocolHandles","termserv.iwtsprotocolconnection_getprotocolhandles","wtsprotocol/IWTSProtocolConnection::GetProtocolHandles"]
old-location: termserv\iwtsprotocolconnection_getprotocolhandles.htm
tech.root: TermServ
ms.assetid: d453ac71-4733-4a68-892c-ffca2d2954c6
ms.date: 12/05/2018
ms.keywords: GetProtocolHandles, GetProtocolHandles method [Remote Desktop Services], GetProtocolHandles method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],GetProtocolHandles method, IWTSProtocolConnection.GetProtocolHandles, IWTSProtocolConnection::GetProtocolHandles, termserv.iwtsprotocolconnection_getprotocolhandles, wtsprotocol/IWTSProtocolConnection::GetProtocolHandles
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWTSProtocolConnection::GetProtocolHandles
 - wtsprotocol/IWTSProtocolConnection::GetProtocolHandles
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolConnection.GetProtocolHandles
---

# IWTSProtocolConnection::GetProtocolHandles


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnection::GetProtocolHandles</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getinputhandles">IWRdsProtocolConnection::GetInputHandles</a> and <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getvideohandle">IWRdsProtocolConnection::GetVideoHandle</a>.]

Retrieves keyboard, mouse, sound, and beep handles supported by the protocol.

## -parameters

### -param pKeyboardHandle [out]

A pointer to a keyboard handle. This is a handle to an <a href="/windows-hardware/drivers/usbcon/winusb-functions-for-pipe-policy-modification">I8042prt keyboard driver</a>.

### -param pMouseHandle [out]

A pointer to a mouse handle. This is a handle to a <a href="/previous-versions/ff542367(v=vs.85)">Mouclass driver</a>.

### -param pBeepHandle [out]

A pointer to a beep device handle. This handle is not used and must be set to <b>NULL</b>.

### -param pVideoHandle [out]

 A pointer to a video device handle. This is a handle to the video miniport driver for the remote session associated with the protocol.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>