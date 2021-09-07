---
UID: NF:wsmandisp.IWSManConnectionOptionsEx2.ProxyAuthenticationUseNegotiate
title: IWSManConnectionOptionsEx2::ProxyAuthenticationUseNegotiate (wsmandisp.h)
description: Returns the value of the proxy authentication flag WSManFlagProxyAuthenticationUseNegotiate for use in the authenticationMechanism parameter of the IWSManConnectionOptionsEx2::SetProxy method.
helpviewer_keywords: ["IWSManConnectionOptionsEx2 interface [Windows Remote Management]","ProxyAuthenticationUseNegotiate method","IWSManConnectionOptionsEx2.ProxyAuthenticationUseNegotiate","IWSManConnectionOptionsEx2::ProxyAuthenticationUseNegotiate","ProxyAuthenticationUseNegotiate","ProxyAuthenticationUseNegotiate method [Windows Remote Management]","ProxyAuthenticationUseNegotiate method [Windows Remote Management]","IWSManConnectionOptionsEx2 interface","winrm.iwsmanconnectionoptionsex2_proxyauthenticationusenegotiate","wsmandisp/IWSManConnectionOptionsEx2::ProxyAuthenticationUseNegotiate"]
old-location: winrm\iwsmanconnectionoptionsex2_proxyauthenticationusenegotiate.htm
tech.root: winrm
ms.assetid: e7dfed5c-7897-4289-bd69-5f6fffaf66f7
ms.date: 12/05/2018
ms.keywords: IWSManConnectionOptionsEx2 interface [Windows Remote Management],ProxyAuthenticationUseNegotiate method, IWSManConnectionOptionsEx2.ProxyAuthenticationUseNegotiate, IWSManConnectionOptionsEx2::ProxyAuthenticationUseNegotiate, ProxyAuthenticationUseNegotiate, ProxyAuthenticationUseNegotiate method [Windows Remote Management], ProxyAuthenticationUseNegotiate method [Windows Remote Management],IWSManConnectionOptionsEx2 interface, winrm.iwsmanconnectionoptionsex2_proxyauthenticationusenegotiate, wsmandisp/IWSManConnectionOptionsEx2::ProxyAuthenticationUseNegotiate
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - IWSManConnectionOptionsEx2::ProxyAuthenticationUseNegotiate
 - wsmandisp/IWSManConnectionOptionsEx2::ProxyAuthenticationUseNegotiate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSManDisp.h
api_name:
 - IWSManConnectionOptionsEx2.ProxyAuthenticationUseNegotiate
---

# IWSManConnectionOptionsEx2::ProxyAuthenticationUseNegotiate


## -description

Returns the value of the proxy authentication flag <b>WSManFlagProxyAuthenticationUseNegotiate</b> for use in the <i>authenticationMechanism</i> parameter of the <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy">IWSManConnectionOptionsEx2::SetProxy</a> method.

## -parameters

### -param value [out, retval]

Specifies the value of the constant.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanconnectionoptionsex2">IWSManConnectionOptionsEx2</a>