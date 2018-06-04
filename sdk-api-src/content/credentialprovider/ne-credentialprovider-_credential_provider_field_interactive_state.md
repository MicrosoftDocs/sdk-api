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

# _CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE enumeration


## -description


Describes the state of a field and how it a user can interact with it. Fields can be displayed by a credential provider in a variety of different interactive states. Used by <a href="https://msdn.microsoft.com/9a709835-cf89-464d-a257-d16a1312ab44">ICredentialProviderCredential::GetFieldState</a> and <a href="https://msdn.microsoft.com/649f0f65-78dd-4232-b471-9a18d1448f1d">ICredentialProviderCredentialEvents::SetFieldInteractiveState</a>.


## -enum-fields




### -field CPFIS_NONE

The field can be edited if the field type supports editing. It also contains none of the other available interactive states.


### -field CPFIS_READONLY

Reserved and not used.


### -field CPFIS_DISABLED

The field is disabled. The user can see it but not interact with it. This support was added starting with Windows 10.


### -field CPFIS_FOCUSED

Credential providers use this field interactive state to indicate that the field should receive initial keyboard focus. This interactive state may not be specified for field types that the user cannot edit. If several editable fields specify this state, the last of them based on <i>dwIndex</i> order receives focus. On systems before  Windows 10, it was the first of editable fields based on <i>dwIndex</i> order. This field interactive state is obeyed only during initial enumeration.


## -remarks



Starting with Windows 10, field interactive states are set during the initial rendering of the Credential UI and when the credential provider fires interactive state change events. An example of this event would be when the user enters digits in the first field and the credential provider automatically moves the cursor to the second field. Be careful when you fire interactive state change events because it could interrupt users entering credential data.



