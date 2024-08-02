---
UID: NF:eappapis.EapHostPeerSetResponseAttributes
title: EapHostPeerSetResponseAttributes function (eappapis.h)
description: Provides updated EAP authentication attributes to EAPHost.
helpviewer_keywords: ["EapHostPeerSetResponseAttributes","EapHostPeerSetResponseAttributes function [EAPHost]","eaphost.eaphostpeersetresponseattributes","eappapis/EapHostPeerSetResponseAttributes"]
old-location: eaphost\eaphostpeersetresponseattributes.htm
tech.root: eaphost
ms.assetid: b8ce5510-f5ba-403c-8709-940ae58cd10d
ms.date: 12/05/2018
ms.keywords: EapHostPeerSetResponseAttributes, EapHostPeerSetResponseAttributes function [EAPHost], eaphost.eaphostpeersetresponseattributes, eappapis/EapHostPeerSetResponseAttributes
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapHostPeerSetResponseAttributes
 - eappapis/EapHostPeerSetResponseAttributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappprxy.dll
api_name:
 - EapHostPeerSetResponseAttributes
---

# EapHostPeerSetResponseAttributes function


## -description

Provides updated EAP authentication attributes to EAPHost.

## -parameters

### -param sessionHandle [in]

A pointer to an <b>EAP_SESSIONID</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionId</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>.

### -param pAttribs [in]

A pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes">EapAttributes</a> structure that contains an array of new EAP authentication response attributes to set for the supplicant on EAPHost.

### -param pEapOutput [out]

A pointer to an <a href="/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction">EapHostPeerResponseAction</a> enumeration value that specifies the action code for the next step the supplicant must take as a response.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. After using the error data, free this memory by calling <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror">EapHostPeerFreeEapError</a>.

## -remarks

To progress to the next step in the state machine after a call to <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes">EapHostPeerGetResponseAttributes</a>, the supplicant must call <b>EapHostPeerSetResponseAttributes</b>. The supplicant must do so to pass a valid <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes">EapAttributes</a>  structure, even if the supplicant cannot use the attributes
returned from <b>EapHostPeerGetResponseAttributes</b>.   

The following example shows a  <b>EapHostPeerSetResponseAttributes</b> call that is made solely to progress to the next state in the state machine. 


``` syntax
EapHostPeerGetResponseAttributes(session_id, &eapAttributes, ppEapError);

// overwrite attributes returned by EapHostPeerGetResponseAttributes
EapAttributes eapAttributes={0,NULL};

// progress to the next state in the state machine
EapHostPeerSetResponseAttributes(session_id, &eapAttributes, pEapOutput, ppEapError);
```


## -see-also

[EAPHost Supplicant Run-time Functions](/windows/win32/eaphost/eap-host-supplicant-run-time-functions)



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes">EapHostPeerGetResponseAttributes</a>
