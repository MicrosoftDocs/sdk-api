---
UID: NE:credentialprovider._CREDENTIAL_PROVIDER_FIELD_STATE
title: CREDENTIAL_PROVIDER_FIELD_STATE (credentialprovider.h)
description: Specifies the state of a single field in the Credential UI.
helpviewer_keywords: ["CPFS_DISPLAY_IN_BOTH","CPFS_DISPLAY_IN_DESELECTED_TILE","CPFS_DISPLAY_IN_SELECTED_TILE","CPFS_HIDDEN","CREDENTIAL_PROVIDER_FIELD_STATE","CREDENTIAL_PROVIDER_FIELD_STATE enumeration [Windows Shell]","credentialprovider/CPFS_DISPLAY_IN_BOTH","credentialprovider/CPFS_DISPLAY_IN_DESELECTED_TILE","credentialprovider/CPFS_DISPLAY_IN_SELECTED_TILE","credentialprovider/CPFS_HIDDEN","credentialprovider/CREDENTIAL_PROVIDER_FIELD_STATE","shell.CREDENTIAL_PROVIDER_FIELD_STATE","shell_CREDENTIAL_PROVIDER_FIELD_STATE"]
old-location: shell\CREDENTIAL_PROVIDER_FIELD_STATE.htm
tech.root: shell
ms.assetid: 4cc7858c-483b-4fac-96ba-8962bc362422
ms.date: 12/05/2018
ms.keywords: CPFS_DISPLAY_IN_BOTH, CPFS_DISPLAY_IN_DESELECTED_TILE, CPFS_DISPLAY_IN_SELECTED_TILE, CPFS_HIDDEN, CREDENTIAL_PROVIDER_FIELD_STATE, CREDENTIAL_PROVIDER_FIELD_STATE enumeration [Windows Shell], credentialprovider/CPFS_DISPLAY_IN_BOTH, credentialprovider/CPFS_DISPLAY_IN_DESELECTED_TILE, credentialprovider/CPFS_DISPLAY_IN_SELECTED_TILE, credentialprovider/CPFS_HIDDEN, credentialprovider/CREDENTIAL_PROVIDER_FIELD_STATE, shell.CREDENTIAL_PROVIDER_FIELD_STATE, shell_CREDENTIAL_PROVIDER_FIELD_STATE
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
req.typenames: CREDENTIAL_PROVIDER_FIELD_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CREDENTIAL_PROVIDER_FIELD_STATE
 - credentialprovider/_CREDENTIAL_PROVIDER_FIELD_STATE
 - CREDENTIAL_PROVIDER_FIELD_STATE
 - credentialprovider/CREDENTIAL_PROVIDER_FIELD_STATE
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
 - CREDENTIAL_PROVIDER_FIELD_STATE
---

# CREDENTIAL_PROVIDER_FIELD_STATE enumeration


## -description

Specifies the state of a single field in the Credential UI. Used by <a href="/windows/win32/api/credentialprovider/ns-credentialprovider-credential_provider_field_descriptor">CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</a> and <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents-setfieldstate">ICredentialProviderCredentialEvents::SetFieldState</a>. The behavior of fields may vary depending on the current field state.

## -enum-fields

### -field CPFS_HIDDEN:0

Do not show the field in any state. One example of this would be a password edit control that should not be displayed until the user authenticates a thumb print. Until the thumb print has been authenticated, the state of the password field would be <b>CPFS_HIDDEN</b>.

### -field CPFS_DISPLAY_IN_SELECTED_TILE

Show the field when in the selected state.

### -field CPFS_DISPLAY_IN_DESELECTED_TILE

Show the field when in the deselected state. This value is only valid for a <a href="/windows/win32/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario">CREDENTIAL_PROVIDER_USAGE_SCENARIO</a> is set to <b>CPUS_CREDUI</b>.

### -field CPFS_DISPLAY_IN_BOTH

Show the field both when the credential tile is selected and when it is not selected.
