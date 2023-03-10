---
UID: NF:webservices.WsFreeListener
title: WsFreeListener function (webservices.h)
description: Releases the memory resource associated with a Listener object.
helpviewer_keywords: ["WsFreeListener","WsFreeListener function [Web Services for Windows]","webservices/WsFreeListener","wsw.wsfreelistener"]
old-location: wsw\wsfreelistener.htm
tech.root: wsw
ms.assetid: 3a8a4cd3-d98e-467b-bbed-5cbd66f892ed
ms.date: 12/05/2018
ms.keywords: WsFreeListener, WsFreeListener function [Web Services for Windows], webservices/WsFreeListener, wsw.wsfreelistener
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - WsFreeListener
 - webservices/WsFreeListener
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
 - WsFreeListener
---

# WsFreeListener function


## -description

Releases the memory resource associated with a Listener object.
            The Listener state represented in <a href="/windows/desktop/api/webservices/ne-webservices-ws_listener_state">WS_LISTENER_STATE</a> must be set to either <b>WS_LISTENER_STATE_CREATED</b> 
                or <b>WS_LISTENER_STATE_CLOSED</b> to be released.
            If a Listener has been successfully opened, then it must be closed 
                using <a href="/windows/desktop/api/webservices/nf-webservices-wscloselistener">WsCloseListener</a> before it is released.

## -parameters

### -param listener [in]

A pointer to the <b>Listener</b> object to release.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-listener">WS_LISTENER</a> returned
                    by <a href="/windows/desktop/api/webservices/nf-webservices-wscreatelistener">WsCreateListener</a>.  The referenced value may not be <b>NULL</b>.