---
UID: NF:webservices.WsResetListener
title: WsResetListener function (webservices.h)
description: Resets a Listener object so it can be reused. Use of this function requires that the Listener state be set to WS_LISTENER_STATE_CREATED or WS_LISTENER_STATE_CLOSED.
helpviewer_keywords: ["WsResetListener","WsResetListener function [Web Services for Windows]","webservices/WsResetListener","wsw.wsresetlistener"]
old-location: wsw\wsresetlistener.htm
tech.root: wsw
ms.assetid: c23c8ad4-a193-42f2-9e4a-3e814b7bbdb2
ms.date: 12/05/2018
ms.keywords: WsResetListener, WsResetListener function [Web Services for Windows], webservices/WsResetListener, wsw.wsresetlistener
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
 - WsResetListener
 - webservices/WsResetListener
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
 - WsResetListener
---

# WsResetListener function


## -description

Resets a Listener object so it can be reused.
            
Use of this function requires that the Listener state be set to <b>WS_LISTENER_STATE_CREATED</b> or <b>WS_LISTENER_STATE_CLOSED</b>.

## -parameters

### -param listener [in]

A pointer to the <b>Listener</b> object to reset.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-listener">WS_LISTENER</a>.

### -param error [in, optional]

A  pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object where additional information about the error should be stored if the function fails.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The listener was in an inappropriate state.
                

</td>
</tr>
</table>

## -remarks

Before reusing a listener, this function should be called.