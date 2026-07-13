---
UID: NE:winnt._SID_NAME_USE
title: SID_NAME_USE (winnt.h)
description: Contains values that specify the type of a security identifier (SID).
helpviewer_keywords: ["*PSID_NAME_USE","PSID_NAME_USE","PSID_NAME_USE enumeration pointer [Security]","SID_NAME_USE","SID_NAME_USE enumeration [Security]","SidTypeAlias","SidTypeComputer","SidTypeDeletedAccount","SidTypeDomain","SidTypeGroup","SidTypeInvalid","SidTypeLabel","SidTypeUnknown","SidTypeUser","SidTypeWellKnownGroup","_win32_sid_name_use_str","security.sid_name_use","winnt/PSID_NAME_USE","winnt/SID_NAME_USE","winnt/SidTypeAlias","winnt/SidTypeComputer","winnt/SidTypeDeletedAccount","winnt/SidTypeDomain","winnt/SidTypeGroup","winnt/SidTypeInvalid","winnt/SidTypeLabel","winnt/SidTypeUnknown","winnt/SidTypeUser","winnt/SidTypeWellKnownGroup"]
old-location: security\sid_name_use.htm
tech.root: security
ms.assetid: 4e6af6bd-056b-4f5a-b223-57a673c3fcfa
ms.date: 12/05/2018
ms.keywords: '*PSID_NAME_USE, PSID_NAME_USE, PSID_NAME_USE enumeration pointer [Security], SID_NAME_USE, SID_NAME_USE enumeration [Security], SidTypeAlias, SidTypeComputer, SidTypeDeletedAccount, SidTypeDomain, SidTypeGroup, SidTypeInvalid, SidTypeLabel, SidTypeUnknown, SidTypeUser, SidTypeWellKnownGroup, _win32_sid_name_use_str, security.sid_name_use, winnt/PSID_NAME_USE, winnt/SID_NAME_USE, winnt/SidTypeAlias, winnt/SidTypeComputer, winnt/SidTypeDeletedAccount, winnt/SidTypeDomain, winnt/SidTypeGroup, winnt/SidTypeInvalid, winnt/SidTypeLabel, winnt/SidTypeUnknown, winnt/SidTypeUser, winnt/SidTypeWellKnownGroup'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SID_NAME_USE, *PSID_NAME_USE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SID_NAME_USE
 - winnt/_SID_NAME_USE
 - PSID_NAME_USE
 - winnt/PSID_NAME_USE
 - SID_NAME_USE
 - winnt/SID_NAME_USE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - SID_NAME_USE
---

# SID_NAME_USE enumeration


## -description

The <b>SID_NAME_USE</b> enumeration contains values that specify the type of a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID).

## -enum-fields

### -field SidTypeUser:1

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

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-enumerations">Authorization Enumerations</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountsida">LookupAccountSid</a>
