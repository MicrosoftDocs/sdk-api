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

# CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS enumeration


## -description


Indicates the type of credential that a credential provider should return to associate with the "Other user" tile. Used by <a href="https://msdn.microsoft.com/A274F799-FB0C-40a7-AB9E-9525F6079C9A">ICredentialProviderUserArray_GetAccountOptions</a>.


## -enum-fields




### -field CPAO_NONE

Default. Do not return a credential to associate with the "Other user" tile.


### -field CPAO_EMPTY_LOCAL

Return a credential to associate with the "Other user" tile. This credential can only be used for a local account.


### -field CPAO_EMPTY_CONNECTED

Return a credential to associate with the "Other user" tile. This credential can only be used for a Microsoft account.


## -see-also




<a href="https://msdn.microsoft.com/A274F799-FB0C-40a7-AB9E-9525F6079C9A">ICredentialProviderUserArray_GetAccountOptions</a>
 

 

