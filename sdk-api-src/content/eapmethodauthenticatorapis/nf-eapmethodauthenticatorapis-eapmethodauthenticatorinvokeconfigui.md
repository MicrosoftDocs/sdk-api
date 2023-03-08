---
UID: NF:eapmethodauthenticatorapis.EapMethodAuthenticatorInvokeConfigUI
title: EapMethodAuthenticatorInvokeConfigUI function (eapmethodauthenticatorapis.h)
description: Defines a function that raises the EAP method's connection configuration user interface dialog box on the client.
helpviewer_keywords: ["EapMethodAuthenticatorInvokeConfigUI","EapMethodAuthenticatorInvokeConfigUI function [EAPHost]","eaphost.eapmethodauthenticatorinvokeconfigui","eapmethodauthenticatorapis/EapMethodAuthenticatorInvokeConfigUI"]
old-location: eaphost\eapmethodauthenticatorinvokeconfigui.htm
tech.root: eaphost
ms.assetid: 6d3083a6-1bd2-4dbf-9f8d-1a6e465188af
ms.date: 12/05/2018
ms.keywords: EapMethodAuthenticatorInvokeConfigUI, EapMethodAuthenticatorInvokeConfigUI function [EAPHost], eaphost.eapmethodauthenticatorinvokeconfigui, eapmethodauthenticatorapis/EapMethodAuthenticatorInvokeConfigUI
req.header: eapmethodauthenticatorapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - EapMethodAuthenticatorInvokeConfigUI
 - eapmethodauthenticatorapis/EapMethodAuthenticatorInvokeConfigUI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - eapmethodauthenticatorapis.h
api_name:
 - EapMethodAuthenticatorInvokeConfigUI
---

# EapMethodAuthenticatorInvokeConfigUI function


## -description

Defines a function that raises the EAP method's connection configuration user interface dialog box on the client.

<b>EapMethodAuthenticatorInvokeConfigUI</b> is a function prototype.

<b>EapHostAuthenticatorInvokeConfigUI</b> must be called on threads that have COM initialized for <a href="/previous-versions/ms810413(v=msdn.10)">Single Threaded Apartment</a>. This can be achieved by calling COM API <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a>; when the supplicant has finished  with the STA thread <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a> must be called before exiting.

## -parameters

### -param pEapMethodType [in]

A pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that contains vendor and author information about the EAP method used for authenticating the connection.

### -param hwndParent [in]

A handle to the parent window which will launch the connection configuration user interface dialog box.

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  EAP authentication session behavior.

### -param pwszMachineName [in]

The name of the target machine being configured. <b>NULL</b> means that the local machine is being configured.

### -param dwSizeOfConfigIn [in]

Specifies the size, in bytes, of <i>pConfigIn</i>. May be set to 0.

### -param pConfigIn [in]

A pointer to a byte buffer that contains configuration elements. The buffer is of size <i>dwSizeOfConfigIn</i>. This parameter can be <b>NULL</b> if <i>dwSizeOfConfigIn</i> is set to 0.

### -param pdwSizeOfConfigOut [out]

Specifies the size, in bytes, of the configuration data returned in <i>ppConfigOut</i>.

### -param ppConfigOut [out]

A pointer to a pointer to a byte buffer that contains updated configuration data from the user. After consuming the data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreememory">EapMethodAuthenticatorFreeMemory</a>.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorfreeerrormemory">EapMethodAuthenticatorFreeErrorMemory</a>.

## -see-also

[EAPHost Authenticator Method Functions](/windows/win32/eaphost/eap-host-authenticator-method-functions)