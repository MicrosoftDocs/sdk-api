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

# _SECPKG_CRED_CLASS enumeration


## -description


Indicates the type of credential used in a client context. The <b>SECPKG_CRED_CLASS</b> enumeration is used in the <a href="https://msdn.microsoft.com/5c2c6d01-5de3-4dd1-9fa2-cce9eadd6902">SecPkgContext_CredInfo</a> structure.


## -enum-fields




### -field SecPkgCredClass_None

No credentials are supplied.


### -field SecPkgCredClass_Ephemeral

Indicates the credentials used to log on to the system.


### -field SecPkgCredClass_PersistedGeneric

Indicates saved credentials that are not target specific.


### -field SecPkgCredClass_PersistedSpecific

Indicates saved credentials that are target specific.


### -field SecPkgCredClass_Explicit




#### - SecPkgCredClass_Explicit = 40

Indicates credentials explicitly supplied by the user.

