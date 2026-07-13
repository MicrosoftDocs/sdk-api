---
UID: NF:wsmandisp.IWSManConnectionOptionsEx2.SetProxy
title: IWSManConnectionOptionsEx2::SetProxy (wsmandisp.h)
description: Sets the proxy information for the session.
helpviewer_keywords: ["IWSManConnectionOptionsEx2 interface [Windows Remote Management]","SetProxy method","IWSManConnectionOptionsEx2.SetProxy","IWSManConnectionOptionsEx2::SetProxy","SetProxy","SetProxy method [Windows Remote Management]","SetProxy method [Windows Remote Management]","IWSManConnectionOptionsEx2 interface","winrm.iwsmanconnectionoptionsex2_setproxy","wsmandisp/IWSManConnectionOptionsEx2::SetProxy"]
old-location: winrm\iwsmanconnectionoptionsex2_setproxy.htm
tech.root: winrm
ms.assetid: b87d5625-c77d-41cb-a75d-a45ba0d3fbe6
ms.date: 12/05/2018
ms.keywords: IWSManConnectionOptionsEx2 interface [Windows Remote Management],SetProxy method, IWSManConnectionOptionsEx2.SetProxy, IWSManConnectionOptionsEx2::SetProxy, SetProxy, SetProxy method [Windows Remote Management], SetProxy method [Windows Remote Management],IWSManConnectionOptionsEx2 interface, winrm.iwsmanconnectionoptionsex2_setproxy, wsmandisp/IWSManConnectionOptionsEx2::SetProxy
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
 - IWSManConnectionOptionsEx2::SetProxy
 - wsmandisp/IWSManConnectionOptionsEx2::SetProxy
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
 - IWSManConnectionOptionsEx2.SetProxy
---

# IWSManConnectionOptionsEx2::SetProxy


## -description

Sets the proxy information for the session.

## -parameters

### -param accessType [in]

Specifies the proxy access type. This parameter must be set to one of the values in the <a href="/windows/desktop/api/wsmandisp/ne-wsmandisp-wsmanproxyaccesstypeflags">WSManProxyAccessTypeFlags</a> enumeration. The default value is <b>WSManProxyWinHttpConfig</b>.

### -param authenticationMechanism [in]

Specifies the authentication mechanism to use for the proxy.  This parameter is optional and the default value is 0. If this parameter is set to 0, the WinRM client chooses either Kerberos or Negotiate. Otherwise, this parameter must be set to one of the values in the <a href="/windows/desktop/api/wsmandisp/ne-wsmandisp-wsmanproxyauthenticationflags">WSManProxyAuthenticationFlags</a> enumeration. The default value from the enumeration is <b>WSManFlagProxyAuthenticationUseNegotiate</b>.

### -param userName [in]

Specifies the user name for proxy authentication. This parameter is optional. If a value is not specified for this parameter, the default credentials are used.

### -param password [in]

Specifies the password for proxy authentication. This parameter is optional. If a value is not specified for this parameter, the default credentials are used.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The default credentials are the credentials under which the current thread is operating.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanconnectionoptionsex2">IWSManConnectionOptionsEx2</a>