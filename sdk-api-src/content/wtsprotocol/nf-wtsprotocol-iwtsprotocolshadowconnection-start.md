---
UID: NF:wtsprotocol.IWTSProtocolShadowConnection.Start
title: IWTSProtocolShadowConnection::Start (wtsprotocol.h)
description: IWTSProtocolShadowConnection::Start is no longer available. Instead, use IWRdsProtocolShadowConnection::Start.
helpviewer_keywords: ["IWTSProtocolShadowConnection interface [Remote Desktop Services]","Start method","IWTSProtocolShadowConnection.Start","IWTSProtocolShadowConnection::Start","Start","Start method [Remote Desktop Services]","Start method [Remote Desktop Services]","IWTSProtocolShadowConnection interface","termserv.iwtsprotocolshadowconnection_start","wtsprotocol/IWTSProtocolShadowConnection::Start"]
old-location: termserv\iwtsprotocolshadowconnection_start.htm
tech.root: TermServ
ms.assetid: 7bfe0c45-551f-47bb-a855-6965fed224dc
ms.date: 12/05/2018
ms.keywords: IWTSProtocolShadowConnection interface [Remote Desktop Services],Start method, IWTSProtocolShadowConnection.Start, IWTSProtocolShadowConnection::Start, Start, Start method [Remote Desktop Services], Start method [Remote Desktop Services],IWTSProtocolShadowConnection interface, termserv.iwtsprotocolshadowconnection_start, wtsprotocol/IWTSProtocolShadowConnection::Start
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
 - IWTSProtocolShadowConnection::Start
 - wtsprotocol/IWTSProtocolShadowConnection::Start
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
 - IWTSProtocolShadowConnection.Start
---

# IWTSProtocolShadowConnection::Start


## -description

<p class="CCE_Message">[<b>IWTSProtocolShadowConnection::Start</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolshadowconnection-start">IWRdsProtocolShadowConnection::Start</a>.]

Notifies the protocol that shadowing has started.

## -parameters

### -param pTargetServerName [in]

A pointer to a string that contains the name of the shadowing server.

### -param TargetSessionId [in]

An integer that specifies the ID of the target session to shadow.

### -param HotKeyVk [in]

The virtual key code of the key that must be pressed to stop shadowing. This key is used in combination with the <i>HotkeyModifiers</i> parameter.

### -param HotkeyModifiers [in]

The virtual modifier that specifies the modifier key to press to stop shadowing. Modifier keys include the Shift, Alt, and Ctrl keys. The modifier key is used in combination with the key signified by the <i>HotKeyVk</i> parameter.

### -param pShadowCallback [in]

A pointer to an <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowcallback">IWTSProtocolShadowCallback</a> interface that the protocol can use to call back into the Remote Desktop Services service.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The Remote Desktop Services service also changes the session state on the shadowed client to reflect the fact that it is being shadowed.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowconnection">IWTSProtocolShadowConnection</a>