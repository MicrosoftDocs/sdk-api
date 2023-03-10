---
UID: NF:wtsprotocol.IWRdsProtocolLogonErrorRedirector.RedirectMessage
title: IWRdsProtocolLogonErrorRedirector::RedirectMessage (wtsprotocol.h)
description: Queries the protocol regarding how to redirect the logon message.
helpviewer_keywords: ["IWRdsProtocolLogonErrorRedirector interface [Remote Desktop Services]","RedirectMessage method","IWRdsProtocolLogonErrorRedirector.RedirectMessage","IWRdsProtocolLogonErrorRedirector::RedirectMessage","RedirectMessage","RedirectMessage method [Remote Desktop Services]","RedirectMessage method [Remote Desktop Services]","IWRdsProtocolLogonErrorRedirector interface","termserv.iwrdsprotocollogonerrorredirector_redirectmessage","wtsprotocol/IWRdsProtocolLogonErrorRedirector::RedirectMessage"]
old-location: termserv\iwrdsprotocollogonerrorredirector_redirectmessage.htm
tech.root: TermServ
ms.assetid: b818e2b0-3d6c-4a56-8175-75b585553520
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolLogonErrorRedirector interface [Remote Desktop Services],RedirectMessage method, IWRdsProtocolLogonErrorRedirector.RedirectMessage, IWRdsProtocolLogonErrorRedirector::RedirectMessage, RedirectMessage, RedirectMessage method [Remote Desktop Services], RedirectMessage method [Remote Desktop Services],IWRdsProtocolLogonErrorRedirector interface, termserv.iwrdsprotocollogonerrorredirector_redirectmessage, wtsprotocol/IWRdsProtocolLogonErrorRedirector::RedirectMessage
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
 - IWRdsProtocolLogonErrorRedirector::RedirectMessage
 - wtsprotocol/IWRdsProtocolLogonErrorRedirector::RedirectMessage
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
 - IWRdsProtocolLogonErrorRedirector.RedirectMessage
---

# IWRdsProtocolLogonErrorRedirector::RedirectMessage


## -description

Queries the protocol regarding how to redirect the logon message.

## -parameters

### -param pszCaption [in]

A pointer to a string that contains the message box caption.

### -param pszMessage [in]

A pointer to a string that contains the logon message.

### -param uType [in]

An integer that contains the message box type. For more information, see the <a href="/windows/desktop/api/winuser/nf-winuser-messagebox">MessageBox</a> function.

### -param pResponse [out]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ne-wtsdefs-wts_logon_error_redirector_response">WRDS_LOGON_ERROR_REDIRECTOR_RESPONSE</a> enumeration that specifies to the Remote Desktop Services service the preferred response for redirecting the logon message.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector">IWRdsProtocolLogonErrorRedirector</a>