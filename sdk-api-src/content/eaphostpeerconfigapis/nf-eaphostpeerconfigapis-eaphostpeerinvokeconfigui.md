---
UID: NF:eaphostpeerconfigapis.EapHostPeerInvokeConfigUI
title: EapHostPeerInvokeConfigUI function (eaphostpeerconfigapis.h)
description: Starts the configuration user interface of the specified EAP method.
helpviewer_keywords: ["EapHostPeerInvokeConfigUI","EapHostPeerInvokeConfigUI function [EAPHost]","eaphost.eaphostpeerinvokeconfigui","eaphostpeerconfigapis/EapHostPeerInvokeConfigUI"]
old-location: eaphost\eaphostpeerinvokeconfigui.htm
tech.root: eaphost
ms.assetid: afb20482-a439-437d-9c8f-c4e87e440113
ms.date: 12/05/2018
ms.keywords: EapHostPeerInvokeConfigUI, EapHostPeerInvokeConfigUI function [EAPHost], eaphost.eaphostpeerinvokeconfigui, eaphostpeerconfigapis/EapHostPeerInvokeConfigUI
req.header: eaphostpeerconfigapis.h
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
req.lib: Eappcfg.lib
req.dll: Eappcfg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapHostPeerInvokeConfigUI
 - eaphostpeerconfigapis/EapHostPeerInvokeConfigUI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappcfg.dll
api_name:
 - EapHostPeerInvokeConfigUI
---

# EapHostPeerInvokeConfigUI function


## -description

Starts the configuration user interface of the specified EAP method.

<b>EapHostPeerInvokeConfigUI</b> must be called on threads that have COM initialized for <a href="/previous-versions/ms810413(v=msdn.10)">Single Threaded Apartment</a> (STA). This can be achieved by calling COM API <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a>; when the supplicant has finished  with the STA thread <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a> must be called before exiting.

## -parameters

### -param hwndParent [in]

The handle of the parent window under which configuration dialog appears.

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  EAP authentication session behavior.

### -param eapMethodType [in]

An <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that specifies the EAP method.

### -param dwSizeOfConfigIn [in]

The size of input configuration. May be set to 0 (zero).

### -param pConfigIn [in]

A pointer to a byte buffer that contains configuration elements. The buffer is of size <i>dwSizeOfConfigIn</i>. This parameter can be <b>NULL</b>, if <i>dwSizeOfConfigIn</i> is set to 0 (zero).

### -param pdwSizeOfConfigOut [out]

A pointer to a DWORD that specifies the size of the buffer pointed to by <i>ppConfigOut</i>.

### -param ppConfigOut [out]

A pointer to a pointer to a byte buffer that contains updated configuration data from the user. After consuming the data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory">EapHostPeerFreeMemory</a>.

### -param ppEapError [out]

A pointer to a pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory">EapHostPeerFreeErrorMemory</a>.

## -see-also

[EAPHost Supplicant Configuration Functions](/windows/win32/eaphost/eap-host-supplicant-configuration-functions)