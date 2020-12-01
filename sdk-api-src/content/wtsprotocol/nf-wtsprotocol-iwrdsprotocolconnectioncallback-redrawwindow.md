---
UID: NF:wtsprotocol.IWRdsProtocolConnectionCallback.RedrawWindow
title: IWRdsProtocolConnectionCallback::RedrawWindow (wtsprotocol.h)
description: Requests that the Remote Desktop Services service redraw the client window.
helpviewer_keywords: ["IWRdsProtocolConnectionCallback interface [Remote Desktop Services]","RedrawWindow method","IWRdsProtocolConnectionCallback.RedrawWindow","IWRdsProtocolConnectionCallback::RedrawWindow","RedrawWindow","RedrawWindow method [Remote Desktop Services]","RedrawWindow method [Remote Desktop Services]","IWRdsProtocolConnectionCallback interface","termserv.iwrdsprotocolconnectioncallback_redrawwindow","wtsprotocol/IWRdsProtocolConnectionCallback::RedrawWindow"]
old-location: termserv\iwrdsprotocolconnectioncallback_redrawwindow.htm
tech.root: TermServ
ms.assetid: 92d52015-c5b9-472e-898b-aca6f6e83620
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolConnectionCallback interface [Remote Desktop Services],RedrawWindow method, IWRdsProtocolConnectionCallback.RedrawWindow, IWRdsProtocolConnectionCallback::RedrawWindow, RedrawWindow, RedrawWindow method [Remote Desktop Services], RedrawWindow method [Remote Desktop Services],IWRdsProtocolConnectionCallback interface, termserv.iwrdsprotocolconnectioncallback_redrawwindow, wtsprotocol/IWRdsProtocolConnectionCallback::RedrawWindow
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
 - IWRdsProtocolConnectionCallback::RedrawWindow
 - wtsprotocol/IWRdsProtocolConnectionCallback::RedrawWindow
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
 - IWRdsProtocolConnectionCallback.RedrawWindow
---

# IWRdsProtocolConnectionCallback::RedrawWindow


## -description

Requests that the Remote Desktop Services service redraw the client window.

## -parameters

### -param rect [in, optional]

A <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_small_rect">WRDS_SMALL_RECT</a> structure that contains the x and y coordinates of the screen to redraw. A value of <b>NULL</b> requests that the entire screen be redrawn.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This method is typically called after the <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnectioncallback-stopscreenupdates">StopScreenUpdates</a> method.

To avoid deadlocks when calling this method:

<ul>
<li>Create a separate thread on which to make the call. Do not make the call from inside any protocol method that you are implementing.</li>
<li>Do not block on this method before replying to another call by the Remote Desktop Services service.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback">IWRdsProtocolConnectionCallback</a>