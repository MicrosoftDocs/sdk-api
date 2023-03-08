---
UID: NF:webservices.WsFreeChannel
title: WsFreeChannel function (webservices.h)
description: Releases the memory resource associated with a Channel object.
helpviewer_keywords: ["WsFreeChannel","WsFreeChannel function [Web Services for Windows]","webservices/WsFreeChannel","wsw.wsfreechannel"]
old-location: wsw\wsfreechannel.htm
tech.root: wsw
ms.assetid: 74e36d19-c6db-4bba-90e3-88a48b6a1fb5
ms.date: 12/05/2018
ms.keywords: WsFreeChannel, WsFreeChannel function [Web Services for Windows], webservices/WsFreeChannel, wsw.wsfreechannel
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsFreeChannel
 - webservices/WsFreeChannel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsFreeChannel
---

# WsFreeChannel function


## -description

Releases the memory resource associated with a Channel object.
            
The <b>Channel</b> must be in the either the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_state">WS_CHANNEL_STATE_CREATED</a> or <b>WS_CHANNEL_STATE_CLOSED</b> state to be released. If a Channel has been successfully opened it must be closed before it can be released.

## -parameters

### -param channel [in]

A pointer to the <b>Channel</b> object to release. The pointer must reference a valid <a href="/windows/desktop/wsw/ws-channel">WS_CHANNEL</a> object returned by <a href="/windows/desktop/api/webservices/nf-webservices-wscreatechannel">WsCreateChannel</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wscreatechannelforlistener">WsCreateChannelForListener</a>. The referenced value may not be <b>NULL</b>.

## -remarks

A channel that is in the process of being accepted/opened cannot be released until the accept/open completes.  Use <a href="/windows/desktop/api/webservices/nf-webservices-wsabortchannel">WsAbortChannel</a> to cancel the accept/open process.