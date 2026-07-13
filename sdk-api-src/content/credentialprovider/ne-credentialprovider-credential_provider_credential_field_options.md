---
UID: NE:credentialprovider.CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS
title: CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS (credentialprovider.h)
description: Provides customization options for a single field in a logon or credential UI.
helpviewer_keywords: ["CPCFO_ENABLE_TOUCH_KEYBOARD_AUTO_INVOKE","CPCFO_NUMBERS_ONLY","CPCFPO_ENABLE_PASSWORD_REVEAL","CPCFPO_IS_EMAIL_ADDRESS","CPCFPO_NONE","CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS","CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS enumeration [Windows Shell]","credentialprovider/CPCFO_ENABLE_TOUCH_KEYBOARD_AUTO_INVOKE","credentialprovider/CPCFO_NUMBERS_ONLY","credentialprovider/CPCFPO_ENABLE_PASSWORD_REVEAL","credentialprovider/CPCFPO_IS_EMAIL_ADDRESS","credentialprovider/CPCFPO_NONE","credentialprovider/CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS","shell.CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS","shell.CREDENTIAL_PROVIDER_USER_ENUM"]
old-location: shell\CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS.htm
tech.root: shell
ms.assetid: 6E8623D0-7FC3-4ccb-B17A-CB12A0508F15
ms.date: 12/05/2018
ms.keywords: CPCFO_ENABLE_TOUCH_KEYBOARD_AUTO_INVOKE, CPCFO_NUMBERS_ONLY, CPCFPO_ENABLE_PASSWORD_REVEAL, CPCFPO_IS_EMAIL_ADDRESS, CPCFPO_NONE, CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS, CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS enumeration [Windows Shell], credentialprovider/CPCFO_ENABLE_TOUCH_KEYBOARD_AUTO_INVOKE, credentialprovider/CPCFO_NUMBERS_ONLY, credentialprovider/CPCFPO_ENABLE_PASSWORD_REVEAL, credentialprovider/CPCFPO_IS_EMAIL_ADDRESS, credentialprovider/CPCFPO_NONE, credentialprovider/CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS, shell.CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS, shell.CREDENTIAL_PROVIDER_USER_ENUM
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CredentialProvider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS
 - credentialprovider/CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CredentialProvider.h
api_name:
 - CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS
---

## -description

Provides customization options for a single field in a logon or credential UI. Used by <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents2-setfieldoptions">ICredentialProviderCredentialEvents2::SetFieldOptions</a> and <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialwithfieldoptions-getfieldoptions">ICredentialProviderCredentialWithFieldOptions::GetFieldOptions</a>.

## -enum-fields

### -field CPCFO_NONE:0

Default. Don't show the "password reveal" glyph, and use the standard on-screen keyboard layout.

### -field CPCFO_ENABLE_PASSWORD_REVEAL:0x1

Display the "password reveal" glyph in a password entry box. When this glyph is held down by the user, the entry in the password box is shown in plain text. The glyph is shown here:

<img alt="Password reveal glyph" src="./images/PasswordReveal.png"/>

### -field CPCFO_IS_EMAIL_ADDRESS:0x2

The field will contain an e-mail address. The on-screen keyboard should be optimized for that input (showing the .com and @ keys on the primary keyboard layout). This option is used with Microsoft account credentials.

### -field CPCFO_ENABLE_TOUCH_KEYBOARD_AUTO_INVOKE:0x4

When enabled, the touch keyboard will be automatically invoked. This should be set only on the <b>CPFG_CREDENTIAL_PROVIDER_LOGO</b> field.

### -field CPCFO_NUMBERS_ONLY:0x8

The field will only allow numerals to be entered. The on-screen keyboard should be optimized for that input (showing only a number keypad on the primary keyboard layout). This should be set only on the <b>CPFT_PASSWORD_TEXT</b> field

### -field CPCFO_SHOW_ENGLISH_KEYBOARD:0x10

Show the English keyboard.

## -see-also

<a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents2-setfieldoptions">ICredentialProviderCredentialEvents2::SetFieldOptions</a>

<a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialwithfieldoptions-getfieldoptions">ICredentialProviderCredentialWithFieldOptions::GetFieldOptions</a>
