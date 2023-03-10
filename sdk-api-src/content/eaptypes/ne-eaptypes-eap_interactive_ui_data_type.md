---
UID: NE:eaptypes._EAP_INTERACTIVE_UI_DATA_TYPE
title: EAP_INTERACTIVE_UI_DATA_TYPE (eaptypes.h)
description: Specifies the set of types of interactive UI context data supplied to certain supplicant API calls.
helpviewer_keywords: ["EAP_INTERACTIVE_UI_DATA_TYPE","EAP_INTERACTIVE_UI_DATA_TYPE enumeration [EAPHost]","EapCredExpiryReq","EapCredExpiryResp","EapCredLogonReq","EapCredLogonResp","EapCredReq","EapCredResp","eaphost.eap_interactive_ui_data_type","eaptypes/EAP_INTERACTIVE_UI_DATA_TYPE","eaptypes/EapCredExpiryReq","eaptypes/EapCredExpiryResp","eaptypes/EapCredLogonReq","eaptypes/EapCredLogonResp","eaptypes/EapCredReq","eaptypes/EapCredResp"]
old-location: eaphost\eap_interactive_ui_data_type.htm
tech.root: eaphost
ms.assetid: 0b3cd58c-9396-4c79-842b-76bf03aa7d7a
ms.date: 12/05/2018
ms.keywords: EAP_INTERACTIVE_UI_DATA_TYPE, EAP_INTERACTIVE_UI_DATA_TYPE enumeration [EAPHost], EapCredExpiryReq, EapCredExpiryResp, EapCredLogonReq, EapCredLogonResp, EapCredReq, EapCredResp, eaphost.eap_interactive_ui_data_type, eaptypes/EAP_INTERACTIVE_UI_DATA_TYPE, eaptypes/EapCredExpiryReq, eaptypes/EapCredExpiryResp, eaptypes/EapCredLogonReq, eaptypes/EapCredLogonResp, eaptypes/EapCredReq, eaptypes/EapCredResp
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
req.typenames: EAP_INTERACTIVE_UI_DATA_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAP_INTERACTIVE_UI_DATA_TYPE
 - eaptypes/_EAP_INTERACTIVE_UI_DATA_TYPE
 - EAP_INTERACTIVE_UI_DATA_TYPE
 - eaptypes/EAP_INTERACTIVE_UI_DATA_TYPE
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
 - EAP_INTERACTIVE_UI_DATA_TYPE
---

# EAP_INTERACTIVE_UI_DATA_TYPE enumeration


## -description

The <b>EAP_INTERACTIVE_UI_DATA_TYPE</b> enumeration specifies the set of types of interactive UI context data supplied to certain supplicant API calls.

## -enum-fields

### -field EapCredReq

The data contains an EAP security credential retry request.

### -field EapCredResp

The data contains an EAP security credential retry response.

### -field EapCredExpiryReq

The data contains an EAP security credential expiration request.

### -field EapCredExpiryResp

The data contains an EAP security credential expiration response.

### -field EapCredLogonReq

The data contains an EAP security credential logon request.

### -field EapCredLogonResp

The data contains an EAP security credential logon response.

## -remarks

The <b>EAP_INTERACTIVE_UI_DATA_TYPE</b> is used to support Single-Sign-On (SSO).

## -see-also

[EAPHost Supplicant Enumerations](/windows/win32/eaphost/eap-host-supplicant-enumerations)



[SSO and PLAP](/windows/win32/eaphost/understanding-sso-and-plap)

