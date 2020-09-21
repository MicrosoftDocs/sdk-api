---
UID: NS:eaptypes._EAP_CRED_EXPIRY_REQ
title: EAP_CRED_EXPIRY_REQ (eaptypes.h)
description: Contains both the old and new EAP credentials for credential expiry operations.
helpviewer_keywords: ["EAP_CRED_EXPIRY_REQ","EAP_CRED_EXPIRY_REQ structure [EAPHost]","EAP_CRED_EXPIRY_RESP","PEAP_CRED_EXPIRY_REQ","PEAP_CRED_EXPIRY_REQ structure pointer [EAPHost]","_EAP_CRED_EXPIRY_REQ","eaphost.eap_cred_expiry_req","eaptypes/EAP_CRED_EXPIRY_REQ","eaptypes/PEAP_CRED_EXPIRY_REQ"]
old-location: eaphost\eap_cred_expiry_req.htm
tech.root: eaphost
ms.assetid: baa2a580-0bfc-450a-9a96-f32d00127fa4
ms.date: 12/05/2018
ms.keywords: EAP_CRED_EXPIRY_REQ, EAP_CRED_EXPIRY_REQ structure [EAPHost], EAP_CRED_EXPIRY_RESP, PEAP_CRED_EXPIRY_REQ, PEAP_CRED_EXPIRY_REQ structure pointer [EAPHost], _EAP_CRED_EXPIRY_REQ, eaphost.eap_cred_expiry_req, eaptypes/EAP_CRED_EXPIRY_REQ, eaptypes/PEAP_CRED_EXPIRY_REQ
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
req.typenames: EAP_CRED_EXPIRY_REQ, EAP_CRED_EXPIRY_RESP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAP_CRED_EXPIRY_REQ
 - eaptypes/_EAP_CRED_EXPIRY_REQ
 - EAP_CRED_EXPIRY_REQ
 - eaptypes/EAP_CRED_EXPIRY_REQ
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
 - EAP_CRED_EXPIRY_REQ
---

# EAP_CRED_EXPIRY_REQ structure


## -description

The <b>EAP_CRED_EXPIRY_REQ</b> structure contains both the old and new EAP credentials for credential expiry operations.

## -struct-fields

### -field curCreds

<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array">EAP_CONFIG_INPUT_FIELD_ARRAY</a> structure that contains the old EAP credentials.

### -field newCreds

<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array">EAP_CONFIG_INPUT_FIELD_ARRAY</a> structure that contains the new EAP credentials.

## -remarks

The <b>EAP_CRED_EXPIRY_REQ</b> structure can be employed to support Single-Sign-On (SSO).

The <b>EAP_CRED_EXPIRY_REQ</b> structure is identical to the <a href="/previous-versions/windows/desktop/legacy/bb530539(v=vs.85)">EAP_CRED_EXPIRY_RESP</a> structure.

## -see-also

[EAPHost Supplicant Structures](/windows/win32/eaphost/eap-host-supplicant-structures)



<a href="/previous-versions/windows/desktop/legacy/bb530539(v=vs.85)">EAP_CRED_EXPIRY_RESP</a>



[EAP_CRED_REQ](/windows/win32/eaphost/eap-cred-req)



[EAP_CRED_RESP](/windows/win32/eaphost/eap-cred-resp)



<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data">EAP_INTERACTIVE_UI_DATA</a>



[SSO and PLAP](/windows/win32/eaphost/understanding-sso-and-plap)