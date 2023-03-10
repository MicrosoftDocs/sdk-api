---
UID: NF:wtsprotocol.IWRdsProtocolShadowConnection.Start
title: IWRdsProtocolShadowConnection::Start (wtsprotocol.h)
description: Notifies the protocol that shadowing has started.
helpviewer_keywords: ["IWRdsProtocolShadowConnection interface [Remote Desktop Services]","Start method","IWRdsProtocolShadowConnection.Start","IWRdsProtocolShadowConnection::Start","Start","Start method [Remote Desktop Services]","Start method [Remote Desktop Services]","IWRdsProtocolShadowConnection interface","termserv.iwrdsprotocolshadowconnection_start","wtsprotocol/IWRdsProtocolShadowConnection::Start"]
old-location: termserv\iwrdsprotocolshadowconnection_start.htm
tech.root: TermServ
ms.assetid: 1f7b5811-6aba-41f2-9fa4-2bbc4c6e005c
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolShadowConnection interface [Remote Desktop Services],Start method, IWRdsProtocolShadowConnection.Start, IWRdsProtocolShadowConnection::Start, Start, Start method [Remote Desktop Services], Start method [Remote Desktop Services],IWRdsProtocolShadowConnection interface, termserv.iwrdsprotocolshadowconnection_start, wtsprotocol/IWRdsProtocolShadowConnection::Start
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - IWRdsProtocolShadowConnection::Start
 - wtsprotocol/IWRdsProtocolShadowConnection::Start
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolShadowConnection.Start
---

# IWRdsProtocolShadowConnection::Start


## -description

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

A pointer to an <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback">IWRdsProtocolShadowCallback</a> interface that the protocol can use to call back into the Remote Desktop Services service.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The Remote Desktop Services service also changes the session state on the shadowed client to reflect the fact that it is being shadowed.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection">IWRdsProtocolShadowConnection</a>