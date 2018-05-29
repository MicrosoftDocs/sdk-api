---
UID: NE:winnt._SID_NAME_USE
title: "_SID_NAME_USE"
author: windows-sdk-content
description: Contains values that specify the type of a security identifier (SID).
old-location: security\sid_name_use.htm
old-project: SecAuthZ
ms.assetid: 4e6af6bd-056b-4f5a-b223-57a673c3fcfa
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*PSID_NAME_USE, PSID_NAME_USE, PSID_NAME_USE enumeration pointer [Security], SID_NAME_USE, SID_NAME_USE enumeration [Security], SidTypeAlias, SidTypeComputer, SidTypeDeletedAccount, SidTypeDomain, SidTypeGroup, SidTypeInvalid, SidTypeLabel, SidTypeUnknown, SidTypeUser, SidTypeWellKnownGroup, _SID_NAME_USE, _win32_sid_name_use_str, security.sid_name_use, winnt/PSID_NAME_USE, winnt/SID_NAME_USE, winnt/SidTypeAlias, winnt/SidTypeComputer, winnt/SidTypeDeletedAccount, winnt/SidTypeDomain, winnt/SidTypeGroup, winnt/SidTypeInvalid, winnt/SidTypeLabel, winnt/SidTypeUnknown, winnt/SidTypeUser, winnt/SidTypeWellKnownGroup"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SID_NAME_USE, *PSID_NAME_USE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winnt.h
api_name:
-	SID_NAME_USE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

