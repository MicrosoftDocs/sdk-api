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

# _SECPKG_NAME_TYPE enumeration


## -description



			The <b>SECPKG_NAME_TYPE</b> enumeration is used to describe the type of name specified for an account.

The <b>SECPKG_NAME_TYPE</b> enumeration is used by the 
<a href="https://msdn.microsoft.com/1cc02c6b-2628-441d-97ae-ed83a4f6bfd0">GetAuthDataForUser</a> and 
<a href="https://msdn.microsoft.com/1d9bfbe5-8dd2-4b0f-a19a-361eef8901a4">OpenSamUser</a> functions.


## -enum-fields




### -field SecNameSamCompatible

The account name is compatible with the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Security Accounts Manager</a> (SAM). An example of a name in SAM-compatible format is <b>"</b><i>ExampleDomain</i><b>\</b><i>UserName</i><b>"</b>.


### -field SecNameAlternateId

The account name is in the AltSecId property of the SAM account.


### -field SecNameFlat

The account name is a flat user principal name (UPN) style account name.


### -field SecNameDN

The account name is the distinguished name of the object.


### -field SecNameSPN



