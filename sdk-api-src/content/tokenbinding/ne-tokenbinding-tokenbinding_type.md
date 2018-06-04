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

# TOKENBINDING_TYPE enumeration


## -description


Specifies the possible types for a token binding.


## -enum-fields




### -field TOKENBINDING_TYPE_PROVIDED

This type of Token Binding is used to protect tokens issued by the Identity Provider for the client to present with subsequent requests back to this Identity Provider.


### -field TOKENBINDING_TYPE_REFERRED

This type of Token Binding is used to protect tokens issued by the Identity Provider for the client to present to a Relying Party.


## -remarks



More information about the use of these Token Binding types can be found in the <b>Token Binding over HTTP Internet</b> draft.




## -see-also




<a href="https://msdn.microsoft.com/4289E3F0-17AC-485B-A326-2C8BECD5CABB">TokenBindingGenerateBinding</a>
 

 

