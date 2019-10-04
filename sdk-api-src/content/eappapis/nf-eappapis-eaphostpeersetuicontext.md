---
UID: NF:eappapis.EapHostPeerSetUIContext
title: EapHostPeerSetUIContext function (eappapis.h)
author: windows-sdk-content
description: Provides a new or updated user interface context to the EAP peer method loaded on EAPHost after the UI has been raised.
old-location: eaphost\eaphostpeersetuicontext.htm
tech.root: eaphost
ms.assetid: f532dd65-d807-4880-9339-ba233e0faa38
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EapHostPeerSetUIContext, EapHostPeerSetUIContext function [EAPHost], eaphost.eaphostpeersetuicontext, eappapis/EapHostPeerSetUIContext
ms.topic: function
f1_keywords:
- eappapis/EapHostPeerSetUIContext
dev_langs:
 - c++
req.header: eappapis.h
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
req.lib: Eappprxy.lib
req.dll: Eappprxy.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- eappprxy.dll
api_name:
- EapHostPeerSetUIContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EapHostPeerSetUIContext function


## -description


Provides a new or updated user interface context to the EAP peer method loaded on EAPHost after the UI has been raised. For more information about raising the UI, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext">EapHostPeerGetUIContext</a>.

<b>EapHostPeerSetUIContext</b> sets the UI context data that was received from a call to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui">EapHostPeerInvokeInteractiveUI</a>.


## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSIONID</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionId</i> parameter in a previous call to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>.


### -param dwSizeOfUIContextData [in]

The size, in bytes, of the user interface context data buffer provided in <i>pUIContextData</i>.


### -param pUIContextData [in]

A pointer to a byte buffer that contains the new supplicant UI context data to be set on EAPHost. The data is returned from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui">EapHostPeerInvokeInteractiveUI</a> OUT parameter.


### -param pEapOutput [out]

A pointer to an <a href="https://docs.microsoft.com/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction">EapHostPeerResponseAction</a> enumeration value that specifies the action code for the next step the supplicant must take as a response.


### -param ppEapError [out]

A pointer to the address of an <a href="https://docs.microsoft.com/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. After using the error data, free this memory by calling <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror">EapHostPeerFreeEapError</a>.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eap-host-supplicant-run-time-functions">EAPHost Supplicant Run-time Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext">EapHostPeerGetUIContext</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui">EapHostPeerInvokeInteractiveUI</a>
 

 

