---
UID: NE:eapauthenticatortypes._EAP_AUTHENTICATOR_SEND_TIMEOUT
title: EAP_AUTHENTICATOR_SEND_TIMEOUT (eapauthenticatortypes.h)
description: Indicates to the authenticator method the amount of time to wait for user input after the packet is sent. The timeout value can be set to none.
helpviewer_keywords: ["EAP_AUTHENTICATOR_SEND_TIMEOUT","EAP_AUTHENTICATOR_SEND_TIMEOUT enumeration [EAPHost]","EAP_AUTHENTICATOR_SEND_TIMEOUT_BASIC","EAP_AUTHENTICATOR_SEND_TIMEOUT_INTERACTIVE","EAP_AUTHENTICATOR_SEND_TIMEOUT_NONE","eapauthenticatortypes/EAP_AUTHENTICATOR_SEND_TIMEOUT","eapauthenticatortypes/EAP_AUTHENTICATOR_SEND_TIMEOUT_BASIC","eapauthenticatortypes/EAP_AUTHENTICATOR_SEND_TIMEOUT_INTERACTIVE","eapauthenticatortypes/EAP_AUTHENTICATOR_SEND_TIMEOUT_NONE","eaphost.eap_authenticator_send_timeout"]
old-location: eaphost\eap_authenticator_send_timeout.htm
tech.root: eaphost
ms.assetid: 56c3da89-eaa8-4ea9-a912-3e15d713ba45
ms.date: 12/05/2018
ms.keywords: EAP_AUTHENTICATOR_SEND_TIMEOUT, EAP_AUTHENTICATOR_SEND_TIMEOUT enumeration [EAPHost], EAP_AUTHENTICATOR_SEND_TIMEOUT_BASIC, EAP_AUTHENTICATOR_SEND_TIMEOUT_INTERACTIVE, EAP_AUTHENTICATOR_SEND_TIMEOUT_NONE, eapauthenticatortypes/EAP_AUTHENTICATOR_SEND_TIMEOUT, eapauthenticatortypes/EAP_AUTHENTICATOR_SEND_TIMEOUT_BASIC, eapauthenticatortypes/EAP_AUTHENTICATOR_SEND_TIMEOUT_INTERACTIVE, eapauthenticatortypes/EAP_AUTHENTICATOR_SEND_TIMEOUT_NONE, eaphost.eap_authenticator_send_timeout
req.header: eapauthenticatortypes.h
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
req.typenames: EAP_AUTHENTICATOR_SEND_TIMEOUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAP_AUTHENTICATOR_SEND_TIMEOUT
 - eapauthenticatortypes/_EAP_AUTHENTICATOR_SEND_TIMEOUT
 - EAP_AUTHENTICATOR_SEND_TIMEOUT
 - eapauthenticatortypes/EAP_AUTHENTICATOR_SEND_TIMEOUT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eapAuthenticatorTypes.h
api_name:
 - EAP_AUTHENTICATOR_SEND_TIMEOUT
---

# EAP_AUTHENTICATOR_SEND_TIMEOUT enumeration


## -description

Indicates to the authenticator method the amount of time to wait for user input after the packet is sent. The timeout value can be set to none.

## -enum-fields

### -field EAP_AUTHENTICATOR_SEND_TIMEOUT_NONE:0

 Sends the packet and never times out; the user can enter a response at any time.

### -field EAP_AUTHENTICATOR_SEND_TIMEOUT_BASIC

Sends the packet and waits for a standard period of time for a response.

### -field EAP_AUTHENTICATOR_SEND_TIMEOUT_INTERACTIVE

Sends the packet and waits for a response for a longer period of time to allow for an interactive session.

## -see-also

[EAPHost Authenticator Method Enumerations](/windows/win32/eaphost/eap-host-authenticator-method-enumerations)

