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

# _SID_NAME_USE enumeration


## -description


The <b>SID_NAME_USE</b> enumeration contains values that specify the type of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID).


## -enum-fields




### -field SidTypeUser

A user SID.


### -field SidTypeGroup

A group SID.


### -field SidTypeDomain

A domain SID.


### -field SidTypeAlias

An alias SID.


### -field SidTypeWellKnownGroup

A SID for a well-known group.


### -field SidTypeDeletedAccount

A SID for a deleted account.


### -field SidTypeInvalid

A SID that is not valid.


### -field SidTypeUnknown

A SID of unknown type.


### -field SidTypeComputer

A SID for a computer.


### -field SidTypeLabel

A mandatory integrity label SID.


### -field SidTypeLogonSession




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="https://msdn.microsoft.com/e2f22838-102e-432c-9c82-06a3e0741374">Authorization Enumerations</a>



<a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a>



<a href="https://msdn.microsoft.com/b8a44ffc-86e1-4f79-ad51-8340da9eaefd">LookupAccountSid</a>
 

 

