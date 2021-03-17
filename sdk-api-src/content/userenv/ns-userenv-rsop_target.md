---
UID: NS:userenv._RSOP_TARGET
title: RSOP_TARGET (userenv.h)
description: The RSOP_TARGET structure contains computer and user information required by the GenerateGroupPolicy function.
helpviewer_keywords: ["*PRSOP_TARGET","PRSOP_TARGET","PRSOP_TARGET structure pointer [Group Policy]","RSOP_TARGET","RSOP_TARGET structure [Group Policy]","_win32_rsop_target_str","policy.rsop_target_str","userenv/PRSOP_TARGET","userenv/RSOP_TARGET"]
old-location: policy\rsop_target_str.htm
tech.root: Policy
ms.assetid: 65b0eb27-fc4a-44d6-843e-965a90dc51e8
ms.date: 12/05/2018
ms.keywords: '*PRSOP_TARGET, PRSOP_TARGET, PRSOP_TARGET structure pointer [Group Policy], RSOP_TARGET, RSOP_TARGET structure [Group Policy], _win32_rsop_target_str, policy.rsop_target_str, userenv/PRSOP_TARGET, userenv/RSOP_TARGET'
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: RSOP_TARGET, *PRSOP_TARGET
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RSOP_TARGET
 - userenv/_RSOP_TARGET
 - PRSOP_TARGET
 - userenv/PRSOP_TARGET
 - RSOP_TARGET
 - userenv/RSOP_TARGET
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Userenv.h
api_name:
 - RSOP_TARGET
---

# RSOP_TARGET structure


## -description

The
    <b>RSOP_TARGET</b> structure contains computer and user information required by the 
<a href="/windows/desktop/api/userenv/nc-userenv-pfngenerategrouppolicy">GenerateGroupPolicy</a> function.

## -struct-fields

### -field pwszAccountName

Pointer to the account name of the computer or the user.

### -field pwszNewSOM

Pointer to the new domain or organizational unit that is the location for the account identified by the <b>pwszAccountName</b> member. This member can be <b>NULL</b>.

### -field psaSecurityGroups

Pointer to a <b>SAFEARRAY</b> that contains a proposed list of new security groups. This member can be <b>NULL</b>. For more information about security groups, see 
<a href="/previous-versions/windows/desktop/Policy/filtering-the-scope-of-a-gpo">Filtering the Scope of a GPO</a> and 
<a href="/windows/desktop/AD/how-security-groups-are-used-in-access-control">How Security Groups are Used in Access Control</a>.

### -field pRsopToken

Pointer to an <b>RSOPTOKEN</b> to use with the 
<a href="/windows/desktop/api/userenv/nf-userenv-rsopaccesscheckbytype">RSoPAccessCheckByType</a> and the 
<a href="/windows/desktop/api/userenv/nf-userenv-rsopfileaccesscheck">RSoPFileAccessCheck</a> functions.

### -field pGPOList

Pointer to a 
<a href="/windows/desktop/api/userenv/ns-userenv-group_policy_objecta">GROUP_POLICY_OBJECT</a> structure containing a linked list of GPOs.

### -field pWbemServices

Specifies the WMI services pointer to the namespace to which the planning mode policy data should be written.

## -see-also

<a href="/windows/desktop/api/userenv/ns-userenv-group_policy_objecta">GROUP_POLICY_OBJECT</a>



<a href="/windows/desktop/api/userenv/nc-userenv-pfngenerategrouppolicy">GenerateGroupPolicy</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy Overview</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-structures">Group Policy Structures</a>



<a href="/windows/desktop/api/userenv/nf-userenv-rsopaccesscheckbytype">RSoPAccessCheckByType</a>



<a href="/windows/desktop/api/userenv/nf-userenv-rsopfileaccesscheck">RSoPFileAccessCheck</a>