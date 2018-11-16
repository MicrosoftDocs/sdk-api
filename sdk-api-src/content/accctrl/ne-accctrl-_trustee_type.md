---
UID: NE:accctrl._TRUSTEE_TYPE
title: "_TRUSTEE_TYPE"
author: windows-sdk-content
description: Values that indicate the type of trustee identified by a TRUSTEE structure.
old-location: security\trustee_type.htm
tech.root: SecAuthZ
ms.assetid: 6519c79d-9cee-4565-a71e-0b81a27c1185
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: TRUSTEE_IS_ALIAS, TRUSTEE_IS_COMPUTER, TRUSTEE_IS_DELETED, TRUSTEE_IS_DOMAIN, TRUSTEE_IS_GROUP, TRUSTEE_IS_INVALID, TRUSTEE_IS_UNKNOWN, TRUSTEE_IS_USER, TRUSTEE_IS_WELL_KNOWN_GROUP, TRUSTEE_TYPE, TRUSTEE_TYPE enumeration [Security], _TRUSTEE_TYPE, _win32_trustee_type_str, accctrl/TRUSTEE_IS_ALIAS, accctrl/TRUSTEE_IS_COMPUTER, accctrl/TRUSTEE_IS_DELETED, accctrl/TRUSTEE_IS_DOMAIN, accctrl/TRUSTEE_IS_GROUP, accctrl/TRUSTEE_IS_INVALID, accctrl/TRUSTEE_IS_UNKNOWN, accctrl/TRUSTEE_IS_USER, accctrl/TRUSTEE_IS_WELL_KNOWN_GROUP, accctrl/TRUSTEE_TYPE, security.trustee_type
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: accctrl.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AccCtrl.h
api_name:
 - TRUSTEE_TYPE
product: Windows
targetos: Windows
req.typenames: TRUSTEE_TYPE
req.redist: 
---

# _TRUSTEE_TYPE enumeration


## -description


The <b>TRUSTEE_TYPE</b> enumeration contains values that indicate the type of trustee identified by a 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure.


## -enum-fields




### -field TRUSTEE_IS_UNKNOWN

The trustee type is unknown, but it may be valid.


### -field TRUSTEE_IS_USER

Indicates a user.


### -field TRUSTEE_IS_GROUP

Indicates a group.


### -field TRUSTEE_IS_DOMAIN

Indicates a domain.


### -field TRUSTEE_IS_ALIAS

Indicates an alias.


### -field TRUSTEE_IS_WELL_KNOWN_GROUP

Indicates a 
<a href="https://msdn.microsoft.com/eb2f95c4-9465-409b-b76c-9ccae1d05eda">well-known group</a>.


### -field TRUSTEE_IS_DELETED

Indicates a deleted account.


### -field TRUSTEE_IS_INVALID

Indicates a trustee type that is not valid.


### -field TRUSTEE_IS_COMPUTER

Indicates a computer.


## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="https://msdn.microsoft.com/e2f22838-102e-432c-9c82-06a3e0741374">Authorization Enumerations</a>



<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a>
 

 

