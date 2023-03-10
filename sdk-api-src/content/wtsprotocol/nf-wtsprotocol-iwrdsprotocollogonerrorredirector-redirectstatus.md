---
UID: NF:wtsprotocol.IWRdsProtocolLogonErrorRedirector.RedirectStatus
title: IWRdsProtocolLogonErrorRedirector::RedirectStatus (wtsprotocol.h)
description: Queries the protocol regarding how to redirect the client logon status update.
helpviewer_keywords: ["IWRdsProtocolLogonErrorRedirector interface [Remote Desktop Services]","RedirectStatus method","IWRdsProtocolLogonErrorRedirector.RedirectStatus","IWRdsProtocolLogonErrorRedirector::RedirectStatus","RedirectStatus","RedirectStatus method [Remote Desktop Services]","RedirectStatus method [Remote Desktop Services]","IWRdsProtocolLogonErrorRedirector interface","termserv.iwrdsprotocollogonerrorredirector_redirectstatus","wtsprotocol/IWRdsProtocolLogonErrorRedirector::RedirectStatus"]
old-location: termserv\iwrdsprotocollogonerrorredirector_redirectstatus.htm
tech.root: TermServ
ms.assetid: f1f6caec-6e26-4508-b19d-ac0e12758b28
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolLogonErrorRedirector interface [Remote Desktop Services],RedirectStatus method, IWRdsProtocolLogonErrorRedirector.RedirectStatus, IWRdsProtocolLogonErrorRedirector::RedirectStatus, RedirectStatus, RedirectStatus method [Remote Desktop Services], RedirectStatus method [Remote Desktop Services],IWRdsProtocolLogonErrorRedirector interface, termserv.iwrdsprotocollogonerrorredirector_redirectstatus, wtsprotocol/IWRdsProtocolLogonErrorRedirector::RedirectStatus
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
 - IWRdsProtocolLogonErrorRedirector::RedirectStatus
 - wtsprotocol/IWRdsProtocolLogonErrorRedirector::RedirectStatus
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
 - IWRdsProtocolLogonErrorRedirector.RedirectStatus
---

# IWRdsProtocolLogonErrorRedirector::RedirectStatus


## -description

Queries the protocol regarding how to redirect the client logon status update.

## -parameters

### -param pszMessage [in]

A pointer to a string that contains the logon status message.

### -param pResponse [out]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ne-wtsdefs-wts_logon_error_redirector_response">WRDS_LOGON_ERROR_REDIRECTOR_RESPONSE</a> enumeration that contains the response.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector">IWRdsProtocolLogonErrorRedirector</a>