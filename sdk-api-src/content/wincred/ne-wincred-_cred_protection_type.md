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

# _CRED_PROTECTION_TYPE enumeration


## -description


The <b>CRED_PROTECTION_TYPE</b> enumeration specifies the security context in which credentials are encrypted when using the <a href="https://msdn.microsoft.com/1e299dfb-2ffe-463c-9e2c-b7774a2216e3">CredProtect</a> function.


## -enum-fields




### -field CredUnprotected

The credentials are not encrypted.


### -field CredUserProtection

The credentials are encrypted and can be decrypted only in the security context in which they were encrypted or in the security context of a trusted component.


### -field CredTrustedProtection

The credentials are encrypted and can only be decrypted by a trusted component.

