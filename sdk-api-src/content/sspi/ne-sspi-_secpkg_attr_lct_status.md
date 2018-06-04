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

# _SECPKG_ATTR_LCT_STATUS enumeration


## -description


Indicates whether the  token from the most recent call to the <a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext</a> function is the last token from the client.

This enumeration is used in the <a href="https://msdn.microsoft.com/ccb2bb4e-3c65-4305-95ad-b9111f3936b5">SecPkgContext_LastClientTokenStatus</a> structure.


## -enum-fields




### -field SecPkgAttrLastClientTokenYes

The token is the last token from the client.


### -field SecPkgAttrLastClientTokenNo

The token is not the last token from the client.


### -field SecPkgAttrLastClientTokenMaybe

It is not known whether the token is the last token from the client.


## -see-also




<a href="https://msdn.microsoft.com/ccb2bb4e-3c65-4305-95ad-b9111f3936b5">SecPkgContext_LastClientTokenStatus</a>
 

 

