---
UID: NF:wtsprotocol.IWTSProtocolLogonErrorRedirector.RedirectMessage
title: IWTSProtocolLogonErrorRedirector::RedirectMessage (wtsprotocol.h)
description: IWTSProtocolLogonErrorRedirector::RedirectMessage is no longer available. Instead, use IWRdsProtocolLogonErrorRedirector::RedirectMessage.
helpviewer_keywords: ["IWTSProtocolLogonErrorRedirector interface [Remote Desktop Services]","RedirectMessage method","IWTSProtocolLogonErrorRedirector.RedirectMessage","IWTSProtocolLogonErrorRedirector::RedirectMessage","RedirectMessage","RedirectMessage method [Remote Desktop Services]","RedirectMessage method [Remote Desktop Services]","IWTSProtocolLogonErrorRedirector interface","termserv.iwtsprotocollogonerrorredirector_redirectmessage","wtsprotocol/IWTSProtocolLogonErrorRedirector::RedirectMessage"]
old-location: termserv\iwtsprotocollogonerrorredirector_redirectmessage.htm
tech.root: TermServ
ms.assetid: 8db3657c-f64f-4e38-832e-5808557f479d
ms.date: 12/05/2018
ms.keywords: IWTSProtocolLogonErrorRedirector interface [Remote Desktop Services],RedirectMessage method, IWTSProtocolLogonErrorRedirector.RedirectMessage, IWTSProtocolLogonErrorRedirector::RedirectMessage, RedirectMessage, RedirectMessage method [Remote Desktop Services], RedirectMessage method [Remote Desktop Services],IWTSProtocolLogonErrorRedirector interface, termserv.iwtsprotocollogonerrorredirector_redirectmessage, wtsprotocol/IWTSProtocolLogonErrorRedirector::RedirectMessage
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
 - IWTSProtocolLogonErrorRedirector::RedirectMessage
 - wtsprotocol/IWTSProtocolLogonErrorRedirector::RedirectMessage
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
 - IWTSProtocolLogonErrorRedirector.RedirectMessage
---

# IWTSProtocolLogonErrorRedirector::RedirectMessage


## -description

<p class="CCE_Message">[<b>IWTSProtocolLogonErrorRedirector::RedirectMessage</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollogonerrorredirector-redirectmessage">IWRdsProtocolLogonErrorRedirector::RedirectMessage</a>.]

Queries the protocol regarding how to redirect the logon message.

## -parameters

### -param pszCaption [in]

A pointer to a string that contains the message box caption.

### -param pszMessage [in]

A pointer to a string that contains the logon message.

### -param uType [in]

An integer that contains the message box type. For more information, see the <b>MessageBox</b> function.

### -param pResponse [out]

A pointer to a <a href="/windows/win32/api/wtsdefs/ne-wtsdefs-wts_logon_error_redirector_response">WTS_LOGON_ERROR_REDIRECTOR_RESPONSE</a> enumeration that specifies to the Remote Desktop Services service the preferred response for redirecting the logon message.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollogonerrorredirector">IWTSProtocolLogonErrorRedirector</a>