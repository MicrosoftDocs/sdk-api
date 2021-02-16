---
UID: NF:wtsprotocol.IWTSProtocolConnectionCallback.DisplayIOCtl
title: IWTSProtocolConnectionCallback::DisplayIOCtl (wtsprotocol.h)
description: IWTSProtocolConnectionCallback::DisplayIOCtl is no longer available.
helpviewer_keywords: ["DisplayIOCtl","DisplayIOCtl method [Remote Desktop Services]","DisplayIOCtl method [Remote Desktop Services]","IWTSProtocolConnectionCallback interface","IWTSProtocolConnectionCallback interface [Remote Desktop Services]","DisplayIOCtl method","IWTSProtocolConnectionCallback.DisplayIOCtl","IWTSProtocolConnectionCallback::DisplayIOCtl","termserv.iwtsprotocolconnectioncallback_displayioctl","wtsprotocol/IWTSProtocolConnectionCallback::DisplayIOCtl"]
old-location: termserv\iwtsprotocolconnectioncallback_displayioctl.htm
tech.root: TermServ
ms.assetid: bd2c4dfe-580d-406b-b03b-628583aeef61
ms.date: 12/05/2018
ms.keywords: DisplayIOCtl, DisplayIOCtl method [Remote Desktop Services], DisplayIOCtl method [Remote Desktop Services],IWTSProtocolConnectionCallback interface, IWTSProtocolConnectionCallback interface [Remote Desktop Services],DisplayIOCtl method, IWTSProtocolConnectionCallback.DisplayIOCtl, IWTSProtocolConnectionCallback::DisplayIOCtl, termserv.iwtsprotocolconnectioncallback_displayioctl, wtsprotocol/IWTSProtocolConnectionCallback::DisplayIOCtl
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
 - IWTSProtocolConnectionCallback::DisplayIOCtl
 - wtsprotocol/IWTSProtocolConnectionCallback::DisplayIOCtl
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
 - IWTSProtocolConnectionCallback.DisplayIOCtl
---

# IWTSProtocolConnectionCallback::DisplayIOCtl


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnectionCallback::DisplayIOCtl</b> is no longer available for use as of Windows Server 2012.]

Requests that the Remote Desktop Services service send data to the display driver loaded in the session.

## -parameters

### -param DisplayIOCtl [in, optional]

A <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_display_ioctl">WTS_DISPLAY_IOCTL</a> structure that contains data to be sent to the display driver loaded in the session.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

To avoid deadlocks when calling this method:

<ul>
<li>Create a separate thread on which to make the call. Do not make the call from inside of any protocol method that you are implementing.</li>
<li>Do not block on this method before replying to another call by the Remote Desktop Services service.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnectioncallback">IWTSProtocolConnectionCallback</a>



<a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_display_ioctl">WTS_DISPLAY_IOCTL</a>