---
UID: NS:winnt._PRIVILEGE_SET
title: PRIVILEGE_SET (winnt.h)
description: Specifies a set of privileges.
helpviewer_keywords: ["*PPRIVILEGE_SET","PPRIVILEGE_SET","PPRIVILEGE_SET structure pointer [Security]","PRIVILEGE_SET","PRIVILEGE_SET structure [Security]","SE_PRIVILEGE_ENABLED","SE_PRIVILEGE_ENABLED_BY_DEFAULT","SE_PRIVILEGE_USED_FOR_ACCESS","_PRIVILEGE_SET","_win32_privilege_set_str","security.privilege_set","winnt/PPRIVILEGE_SET","winnt/PRIVILEGE_SET"]
old-location: security\privilege_set.htm
tech.root: security
ms.assetid: 2ee5615c-f684-4062-a6cb-e43e9de3a2fb
ms.date: 12/05/2018
ms.keywords: '*PPRIVILEGE_SET, PPRIVILEGE_SET, PPRIVILEGE_SET structure pointer [Security], PRIVILEGE_SET, PRIVILEGE_SET structure [Security], SE_PRIVILEGE_ENABLED, SE_PRIVILEGE_ENABLED_BY_DEFAULT, SE_PRIVILEGE_USED_FOR_ACCESS, _PRIVILEGE_SET, _win32_privilege_set_str, security.privilege_set, winnt/PPRIVILEGE_SET, winnt/PRIVILEGE_SET'
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
req.typenames: PRIVILEGE_SET, *PPRIVILEGE_SET
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PRIVILEGE_SET
 - winnt/_PRIVILEGE_SET
 - PPRIVILEGE_SET
 - winnt/PPRIVILEGE_SET
 - PRIVILEGE_SET
 - winnt/PRIVILEGE_SET
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
 - PRIVILEGE_SET
---

# PRIVILEGE_SET structure


## -description

The <b>PRIVILEGE_SET</b> structure specifies a set of <a href="/windows/desktop/SecGloss/p-gly">privileges</a>. It is also used to indicate which, if any, privileges are held by a user or group requesting access to an object.

## -struct-fields

### -field PrivilegeCount

Specifies the number of privileges in the privilege set.

### -field Control

Specifies a control flag related to the privileges. The PRIVILEGE_SET_ALL_NECESSARY control flag is currently defined. It indicates that all of the specified privileges must be held by the <a href="/windows/desktop/SecGloss/p-gly">process</a> requesting access. If this flag is not set, the presence of any privileges in the user's <a href="/windows/desktop/SecGloss/a-gly">access token</a> grants the access.

### -field Privilege

Specifies an array of 
<a href="/windows/desktop/api/winnt/ns-winnt-luid_and_attributes">LUID_AND_ATTRIBUTES</a> structures describing the set's privileges. The following attributes are defined for privileges. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SE_PRIVILEGE_ENABLED_BY_DEFAULT"></a><a id="se_privilege_enabled_by_default"></a><dl>
<dt><b>SE_PRIVILEGE_ENABLED_BY_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The privilege is enabled by default.

</td>
</tr>
<tr>
<td width="40%"><a id="SE_PRIVILEGE_ENABLED"></a><a id="se_privilege_enabled"></a><dl>
<dt><b>SE_PRIVILEGE_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
The privilege is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="SE_PRIVILEGE_USED_FOR_ACCESS"></a><a id="se_privilege_used_for_access"></a><dl>
<dt><b>SE_PRIVILEGE_USED_FOR_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
The privilege was used to gain access to an object or service. This flag is used to identify the relevant privileges in a set passed by a client application that may contain unnecessary privileges.

</td>
</tr>
</table>

## -remarks

A privilege is used to control access to an object or service more strictly than is typical with discretionary access control. A system manager uses privileges to control which users are able to manipulate system resources. An application uses privileges when it changes a system-wide resource, such as when it changes the system time or shuts down the system.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a>



<a href="/windows/desktop/api/winnt/ns-winnt-luid_and_attributes">LUID_AND_ATTRIBUTES</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-privilegecheck">PrivilegeCheck</a>