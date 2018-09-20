---
UID: NE:credentialprovider._CREDENTIAL_PROVIDER_FIELD_STATE
title: "_CREDENTIAL_PROVIDER_FIELD_STATE"
author: windows-sdk-content
description: Specifies the state of a single field in the Credential UI.
old-location: shell\CREDENTIAL_PROVIDER_FIELD_STATE.htm
tech.root: shell
ms.assetid: 4cc7858c-483b-4fac-96ba-8962bc362422
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: CPFS_DISPLAY_IN_BOTH, CPFS_DISPLAY_IN_DESELECTED_TILE, CPFS_DISPLAY_IN_SELECTED_TILE, CPFS_HIDDEN, CREDENTIAL_PROVIDER_FIELD_STATE, CREDENTIAL_PROVIDER_FIELD_STATE enumeration [Windows Shell], _CREDENTIAL_PROVIDER_FIELD_STATE, credentialprovider/CPFS_DISPLAY_IN_BOTH, credentialprovider/CPFS_DISPLAY_IN_DESELECTED_TILE, credentialprovider/CPFS_DISPLAY_IN_SELECTED_TILE, credentialprovider/CPFS_HIDDEN, credentialprovider/CREDENTIAL_PROVIDER_FIELD_STATE, shell.CREDENTIAL_PROVIDER_FIELD_STATE, shell_CREDENTIAL_PROVIDER_FIELD_STATE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Credentialprovider.h
api_name:
 - CREDENTIAL_PROVIDER_FIELD_STATE
product: Windows
targetos: Windows
req.typenames: CREDENTIAL_PROVIDER_FIELD_STATE
req.redist: 
---

# _CREDENTIAL_PROVIDER_FIELD_STATE enumeration


## -description


Specifies the state of a single field in the Credential UI. Used by <a href="https://msdn.microsoft.com/8409b4b7-c601-4e85-95f9-4272feb29028">CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</a> and <a href="https://msdn.microsoft.com/d3498bca-cc31-4a80-9f31-e1e6d020d777">ICredentialProviderCredentialEvents::SetFieldState</a>. The behavior of fields may vary depending on the current field state.


## -enum-fields




### -field CPFS_HIDDEN

Do not show the field in any state. One example of this would be a password edit control that should not be displayed until the user authenticates a thumb print. Until the thumb print has been authenticated, the state of the password field would be <b>CPFS_HIDDEN</b>.


### -field CPFS_DISPLAY_IN_SELECTED_TILE

Show the field when in the selected state.


### -field CPFS_DISPLAY_IN_DESELECTED_TILE

Show the field when in the deselected state. This value is only valid for a <a href="https://msdn.microsoft.com/86025d1d-b13d-4f61-824a-fd471e449567">CREDENTIAL_PROVIDER_USAGE_SCENARIO</a> is set to <b>CPUS_CREDUI</b>.


### -field CPFS_DISPLAY_IN_BOTH

Show the field both when the credential tile is selected and when it is not selected.

