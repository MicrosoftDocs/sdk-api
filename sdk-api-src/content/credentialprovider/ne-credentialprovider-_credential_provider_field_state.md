---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

