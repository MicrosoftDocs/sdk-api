---
UID: NE:credentialprovider._CREDENTIAL_PROVIDER_FIELD_TYPE
title: CREDENTIAL_PROVIDER_FIELD_TYPE (credentialprovider.h)
description: Specifies a type of credential field. Used by CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR.
helpviewer_keywords: ["CPFT_CHECKBOX","CPFT_COMBOBOX","CPFT_COMMAND_LINK","CPFT_EDIT_TEXT","CPFT_INVALID","CPFT_LARGE_TEXT","CPFT_PASSWORD_TEXT","CPFT_SMALL_TEXT","CPFT_SUBMIT_BUTTON","CPFT_TILE_IMAGE","CREDENTIAL_PROVIDER_FIELD_TYPE","CREDENTIAL_PROVIDER_FIELD_TYPE enumeration [Windows Shell]","credentialprovider/CPFT_CHECKBOX","credentialprovider/CPFT_COMBOBOX","credentialprovider/CPFT_COMMAND_LINK","credentialprovider/CPFT_EDIT_TEXT","credentialprovider/CPFT_INVALID","credentialprovider/CPFT_LARGE_TEXT","credentialprovider/CPFT_PASSWORD_TEXT","credentialprovider/CPFT_SMALL_TEXT","credentialprovider/CPFT_SUBMIT_BUTTON","credentialprovider/CPFT_TILE_IMAGE","credentialprovider/CREDENTIAL_PROVIDER_FIELD_TYPE","shell.CREDENTIAL_PROVIDER_FIELD_TYPE","shell_CREDENTIAL_PROVIDER_FIELD_TYPE"]
old-location: shell\CREDENTIAL_PROVIDER_FIELD_TYPE.htm
tech.root: shell
ms.assetid: 5af9f007-9588-4574-a5ce-3f01ec0b45e8
ms.date: 12/05/2018
ms.keywords: CPFT_CHECKBOX, CPFT_COMBOBOX, CPFT_COMMAND_LINK, CPFT_EDIT_TEXT, CPFT_INVALID, CPFT_LARGE_TEXT, CPFT_PASSWORD_TEXT, CPFT_SMALL_TEXT, CPFT_SUBMIT_BUTTON, CPFT_TILE_IMAGE, CREDENTIAL_PROVIDER_FIELD_TYPE, CREDENTIAL_PROVIDER_FIELD_TYPE enumeration [Windows Shell], credentialprovider/CPFT_CHECKBOX, credentialprovider/CPFT_COMBOBOX, credentialprovider/CPFT_COMMAND_LINK, credentialprovider/CPFT_EDIT_TEXT, credentialprovider/CPFT_INVALID, credentialprovider/CPFT_LARGE_TEXT, credentialprovider/CPFT_PASSWORD_TEXT, credentialprovider/CPFT_SMALL_TEXT, credentialprovider/CPFT_SUBMIT_BUTTON, credentialprovider/CPFT_TILE_IMAGE, credentialprovider/CREDENTIAL_PROVIDER_FIELD_TYPE, shell.CREDENTIAL_PROVIDER_FIELD_TYPE, shell_CREDENTIAL_PROVIDER_FIELD_TYPE
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
req.typenames: CREDENTIAL_PROVIDER_FIELD_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CREDENTIAL_PROVIDER_FIELD_TYPE
 - credentialprovider/_CREDENTIAL_PROVIDER_FIELD_TYPE
 - CREDENTIAL_PROVIDER_FIELD_TYPE
 - credentialprovider/CREDENTIAL_PROVIDER_FIELD_TYPE
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
 - CREDENTIAL_PROVIDER_FIELD_TYPE
---

# CREDENTIAL_PROVIDER_FIELD_TYPE enumeration


## -description

Specifies a type of credential field. Used by <a href="/windows/win32/api/credentialprovider/ns-credentialprovider-credential_provider_field_descriptor">CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</a>.

## -enum-fields

### -field CPFT_INVALID:0

The value is invalid. This is a safe initialization value, as fields do not default to any given type.

### -field CPFT_LARGE_TEXT

A stand-alone text label is drawn in the larger of two font sizes.

### -field CPFT_SMALL_TEXT

A stand-alone text label is drawn in the smaller of two font sizes.

### -field CPFT_COMMAND_LINK

An uneditable string that a user may click to perform an action. The credential provider is informed of the user's click, and then performs the requested action. Use <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-commandlinkclicked">CommandLinkClicked</a> in your credential provider to respond to the click.

### -field CPFT_EDIT_TEXT

An edit box. Users may provide credential information by typing in this box.

### -field CPFT_PASSWORD_TEXT

A special edit control that displays its string as a series of password characters, such as the asterisk character (*). Otherwise this functions the same as <b>CPFT_EDIT_TEXT</b>.

### -field CPFT_TILE_IMAGE

A bitmap that is shown as the user tile image. This bitmap cannot be edited. All credential providers must contain no more than one <b>CPFT_TILE_IMAGE</b>. If no image is specified, Logon UI and Credential UI will supply a default tile image.

### -field CPFT_CHECKBOX

A checkbox control that allows for checked and unchecked states.

### -field CPFT_COMBOBOX

A combobox control that allows users to select an option from a defined set of choices.

### -field CPFT_SUBMIT_BUTTON

This field appears as a button on the credential tile. Pressing the button lets the user submit their credentials. There is exactly one <b>CPFT_SUBMIT_BUTTON</b> on any credential tile. Unlike Logon UI, which draws a special submit button in the tile layout, Credential UI hides this field and renders a single submit button for all credentials.

## -remarks

This type enables you to specify the different elements your credential provider will need to display to the user. Credential providers are not responsible for drawing their own UI, so they need to define the elements that are necessary. This type is one of the elements to support that mechanism.
