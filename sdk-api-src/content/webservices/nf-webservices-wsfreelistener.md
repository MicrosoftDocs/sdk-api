---
UID: NF:webservices.WsFreeListener
title: WsFreeListener function (webservices.h)

description: Releases the memory resource associated with a Listener object.
old-location: wsw\wsfreelistener.htm
tech.root: wsw
ms.assetid: 3a8a4cd3-d98e-467b-bbed-5cbd66f892ed

ms.date: 12/05/2018
ms.keywords: WsFreeListener, WsFreeListener function [Web Services for Windows], webservices/WsFreeListener, wsw.wsfreelistener
ms.topic: function
f1_keywords: 
 - "webservices/WsFreeListener"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsFreeListener
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WsFreeListener function


## -description


Releases the memory resource associated with a Listener object.
            The Listener state represented in <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_listener_state">WS_LISTENER_STATE</a> must be set to either <b>WS_LISTENER_STATE_CREATED</b> 
                or <b>WS_LISTENER_STATE_CLOSED</b> to be released.
            If a Listener has been successfully opened, then it must be closed 
                using <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wscloselistener">WsCloseListener</a> before it is released.


## -parameters




### -param listener [in]

A pointer to the <b>Listener</b> object to release.  The pointer must reference a valid <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-listener">WS_LISTENER</a> returned
                    by <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wscreatelistener">WsCreateListener</a>.  The referenced value may not be <b>NULL</b>.
                


## -returns



This function does not return a value.



