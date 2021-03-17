---
UID: NE:eaptypes._EAP_CONFIG_INPUT_FIELD_TYPE
title: EAP_CONFIG_INPUT_FIELD_TYPE (eaptypes.h)
description: Defines a set of possible input field types available when querying for user credentials.
helpviewer_keywords: ["*PEAP_CONFIG_INPUT_FIELD_TYPE","EAP_CONFIG_INPUT_FIELD_TYPE","EAP_CONFIG_INPUT_FIELD_TYPE enumeration [EAPHost]","EapConfigInputEdit","EapConfigInputNetworkPassword","EapConfigInputNetworkUsername","EapConfigInputPSK","EapConfigInputPassword","EapConfigInputPin","EapConfigInputUsername","EapConfigSmartCardError","EapConfigSmartCardUsername","eaphost.eap_config_input_field_type","eaptypes/EAP_CONFIG_INPUT_FIELD_TYPE","eaptypes/EapConfigInputEdit","eaptypes/EapConfigInputNetworkPassword","eaptypes/EapConfigInputNetworkUsername","eaptypes/EapConfigInputPSK","eaptypes/EapConfigInputPassword","eaptypes/EapConfigInputPin","eaptypes/EapConfigInputUsername","eaptypes/EapConfigSmartCardError","eaptypes/EapConfigSmartCardUsername"]
old-location: eaphost\eap_config_input_field_type.htm
tech.root: eaphost
ms.assetid: f05242ad-1e49-4a6d-b4f1-579c4b00ea28
ms.date: 12/05/2018
ms.keywords: '*PEAP_CONFIG_INPUT_FIELD_TYPE, EAP_CONFIG_INPUT_FIELD_TYPE, EAP_CONFIG_INPUT_FIELD_TYPE enumeration [EAPHost], EapConfigInputEdit, EapConfigInputNetworkPassword, EapConfigInputNetworkUsername, EapConfigInputPSK, EapConfigInputPassword, EapConfigInputPin, EapConfigInputUsername, EapConfigSmartCardError, EapConfigSmartCardUsername, eaphost.eap_config_input_field_type, eaptypes/EAP_CONFIG_INPUT_FIELD_TYPE, eaptypes/EapConfigInputEdit, eaptypes/EapConfigInputNetworkPassword, eaptypes/EapConfigInputNetworkUsername, eaptypes/EapConfigInputPSK, eaptypes/EapConfigInputPassword, eaptypes/EapConfigInputPin, eaptypes/EapConfigInputUsername, eaptypes/EapConfigSmartCardError, eaptypes/EapConfigSmartCardUsername'
req.header: eaptypes.h
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
req.typenames: EAP_CONFIG_INPUT_FIELD_TYPE, *PEAP_CONFIG_INPUT_FIELD_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAP_CONFIG_INPUT_FIELD_TYPE
 - eaptypes/_EAP_CONFIG_INPUT_FIELD_TYPE
 - PEAP_CONFIG_INPUT_FIELD_TYPE
 - eaptypes/PEAP_CONFIG_INPUT_FIELD_TYPE
 - EAP_CONFIG_INPUT_FIELD_TYPE
 - eaptypes/EAP_CONFIG_INPUT_FIELD_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eaptypes.h
api_name:
 - EAP_CONFIG_INPUT_FIELD_TYPE
---

# EAP_CONFIG_INPUT_FIELD_TYPE enumeration


## -description

 The <b>EAP_CONFIG_INPUT_FIELD_TYPE</b> enumeration defines a set of possible  input field types available when querying for user credentials.

## -enum-fields

### -field EapConfigInputUsername

The input field contains a user's application logon name.

### -field EapConfigInputPassword

The input field contains a user's application logon password.

### -field EapConfigInputNetworkUsername

The input field contains a user's network logon name. This is used as an alternate logon user name for <b>EapConfigInputUsername</b>.

### -field EapConfigInputNetworkPassword

The input field contains a user's network login password. This is used as an alternate logon password for <b>EapConfigInputPassword</b>.

### -field EapConfigInputPin

The input field contains the user's network access PIN.

### -field EapConfigInputPSK

The input field contains the user's Flexible Authentication via Secure Tunneling (EAP-FAST) Pre-Shared Key(PSK).

### -field EapConfigInputEdit

The input field contains a generic logon token string.

### -field EapConfigSmartCardUsername

Windows 7 or later: The input field contains the username from a  smartcard certificate.

### -field EapConfigSmartCardError

Windows 7 or later: If an authentication using a smartcard did not succeed in the previous attempt of the current session, this input field contains an error message citing the failure reason.

## -remarks

The <b>EAP_CONFIG_INPUT_FIELD_TYPE</b> enumeration can be employed to support Single-Sign-On (SSO).

## -see-also

[Common EAPHost API Enumerations](/windows/win32/eaphost/common-eap-host-api-enumerations)



[SSO and PLAP](/windows/win32/eaphost/understanding-sso-and-plap)

