---
UID: NF:wtsprotocol.IWTSProtocolLogonErrorRedirector.RedirectStatus
title: IWTSProtocolLogonErrorRedirector::RedirectStatus (wtsprotocol.h)
description: IWTSProtocolLogonErrorRedirector::RedirectStatus is no longer available. Instead, use IWRdsProtocolLogonErrorRedirector::RedirectStatus.
helpviewer_keywords: ["IWTSProtocolLogonErrorRedirector interface [Remote Desktop Services]","RedirectStatus method","IWTSProtocolLogonErrorRedirector.RedirectStatus","IWTSProtocolLogonErrorRedirector::RedirectStatus","RedirectStatus","RedirectStatus method [Remote Desktop Services]","RedirectStatus method [Remote Desktop Services]","IWTSProtocolLogonErrorRedirector interface","termserv.iwtsprotocollogonerrorredirector_redirectstatus","wtsprotocol/IWTSProtocolLogonErrorRedirector::RedirectStatus"]
old-location: termserv\iwtsprotocollogonerrorredirector_redirectstatus.htm
tech.root: TermServ
ms.assetid: a333db5a-3564-4d33-bfd6-244975cc3c4f
ms.date: 12/05/2018
ms.keywords: IWTSProtocolLogonErrorRedirector interface [Remote Desktop Services],RedirectStatus method, IWTSProtocolLogonErrorRedirector.RedirectStatus, IWTSProtocolLogonErrorRedirector::RedirectStatus, RedirectStatus, RedirectStatus method [Remote Desktop Services], RedirectStatus method [Remote Desktop Services],IWTSProtocolLogonErrorRedirector interface, termserv.iwtsprotocollogonerrorredirector_redirectstatus, wtsprotocol/IWTSProtocolLogonErrorRedirector::RedirectStatus
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
 - IWTSProtocolLogonErrorRedirector::RedirectStatus
 - wtsprotocol/IWTSProtocolLogonErrorRedirector::RedirectStatus
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
 - IWTSProtocolLogonErrorRedirector.RedirectStatus
---

# IWTSProtocolLogonErrorRedirector::RedirectStatus


## -description

<p class="CCE_Message">[<b>IWTSProtocolLogonErrorRedirector::RedirectStatus</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollogonerrorredirector-redirectstatus">IWRdsProtocolLogonErrorRedirector::RedirectStatus</a>.]

Queries the protocol regarding how to redirect the client logon status update.

## -parameters

### -param pszMessage [in]

A pointer to a string that contains the logon status message.

### -param pResponse [out]

A pointer to a <a href="/windows/win32/api/wtsdefs/ne-wtsdefs-wts_logon_error_redirector_response">WTS_LOGON_ERROR_REDIRECTOR_RESPONSE</a> enumeration that contains the response. This can be one of the following values.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollogonerrorredirector">IWTSProtocolLogonErrorRedirector</a>