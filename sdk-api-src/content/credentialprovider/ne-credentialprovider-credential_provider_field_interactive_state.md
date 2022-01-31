---
UID: NE:credentialprovider._CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE
title: CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE (credentialprovider.h)
description: Describes the state of a field and how it a user can interact with it. Fields can be displayed by a credential provider in a variety of different interactive states.
helpviewer_keywords: ["CPFIS_DISABLED","CPFIS_FOCUSED","CPFIS_NONE","CPFIS_READONLY","CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE","CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE enumeration [Windows Shell]","_shell_CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE","credentialprovider/CPFIS_DISABLED","credentialprovider/CPFIS_FOCUSED","credentialprovider/CPFIS_NONE","credentialprovider/CPFIS_READONLY","credentialprovider/CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE","shell.CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE"]
old-location: shell\CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE.htm
tech.root: shell
ms.assetid: 745ac5f0-fcfe-4f42-ab4c-c933f1d3870b
ms.date: 12/05/2018
ms.keywords: CPFIS_DISABLED, CPFIS_FOCUSED, CPFIS_NONE, CPFIS_READONLY, CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE, CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE enumeration [Windows Shell], _shell_CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE, credentialprovider/CPFIS_DISABLED, credentialprovider/CPFIS_FOCUSED, credentialprovider/CPFIS_NONE, credentialprovider/CPFIS_READONLY, credentialprovider/CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE, shell.CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Credentialprovider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE
 - credentialprovider/_CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE
 - CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE
 - credentialprovider/CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Credentialprovider.h
api_name:
 - CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE
---

# CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE enumeration


## -description

Describes the state of a field and how it a user can interact with it. Fields can be displayed by a credential provider in a variety of different interactive states. Used by <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-getfieldstate">ICredentialProviderCredential::GetFieldState</a> and <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents-setfieldinteractivestate">ICredentialProviderCredentialEvents::SetFieldInteractiveState</a>.

## -enum-fields

### -field CPFIS_NONE:0

The field can be edited if the field type supports editing. It also contains none of the other available interactive states.

### -field CPFIS_READONLY

Reserved and not used.

### -field CPFIS_DISABLED

The field is disabled. The user can see it but not interact with it. This support was added starting with Windows 10.

### -field CPFIS_FOCUSED

Credential providers use this field interactive state to indicate that the field should receive initial keyboard focus. This interactive state may not be specified for field types that the user cannot edit. If several editable fields specify this state, the last of them based on <i>dwIndex</i> order receives focus. On systems before  Windows 10, it was the first of editable fields based on <i>dwIndex</i> order. This field interactive state is obeyed only during initial enumeration.

## -remarks

Starting with Windows 10, field interactive states are set during the initial rendering of the Credential UI and when the credential provider fires interactive state change events. An example of this event would be when the user enters digits in the first field and the credential provider automatically moves the cursor to the second field. Be careful when you fire interactive state change events because it could interrupt users entering credential data.
