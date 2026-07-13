---
UID: NS:accctrl._TRUSTEE_A
title: TRUSTEE_A (accctrl.h)
description: Identifies the user account, group account, or logon session to which an access control entry (ACE) applies. (ANSI)
helpviewer_keywords: ["*PTRUSTEEA","*PTRUSTEE_A","PTRUSTEE","PTRUSTEE structure pointer [Security]","TRUSTEE","TRUSTEE structure [Security]","TRUSTEEA","TRUSTEE_","TRUSTEE_A","TRUSTEE_IS_NAME","TRUSTEE_IS_OBJECTS_AND_NAME","TRUSTEE_IS_OBJECTS_AND_SID","TRUSTEE_IS_SID","TRUSTEE_W","_win32_trustee_str","accctrl/PTRUSTEE","accctrl/TRUSTEE","accctrl/TRUSTEE_A","accctrl/TRUSTEE_W","security.trustee"]
old-location: security\trustee.htm
tech.root: security
ms.assetid: 120e93eb-680f-4f86-879d-bc2de10d4641
ms.date: 12/05/2018
ms.keywords: '*PTRUSTEEA, *PTRUSTEE_A, PTRUSTEE, PTRUSTEE structure pointer [Security], TRUSTEE, TRUSTEE structure [Security], TRUSTEEA, TRUSTEE_, TRUSTEE_A, TRUSTEE_IS_NAME, TRUSTEE_IS_OBJECTS_AND_NAME, TRUSTEE_IS_OBJECTS_AND_SID, TRUSTEE_IS_SID, TRUSTEE_W, _win32_trustee_str, accctrl/PTRUSTEE, accctrl/TRUSTEE, accctrl/TRUSTEE_A, accctrl/TRUSTEE_W, security.trustee'
req.header: accctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TRUSTEE_W (Unicode) and TRUSTEE_A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TRUSTEE_A, *PTRUSTEE_A, TRUSTEEA, *PTRUSTEEA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TRUSTEE_A
 - accctrl/_TRUSTEE_A
 - PTRUSTEE_A
 - accctrl/PTRUSTEE_A
 - TRUSTEE_A
 - accctrl/TRUSTEE_A
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AccCtrl.h
api_name:
 - TRUSTEE
 - TRUSTEE_A
 - TRUSTEE_W
---

# TRUSTEE_A structure

## -syntax

```cpp
typedef struct _TRUSTEE_A {
  struct _TRUSTEE_A          *pMultipleTrustee;
  MULTIPLE_TRUSTEE_OPERATION MultipleTrusteeOperation;
  TRUSTEE_FORM               TrusteeForm;
  TRUSTEE_TYPE               TrusteeType;
  LPCH                       ptstrName;
} TRUSTEE_A, *PTRUSTEE_A, TRUSTEEA, *PTRUSTEEA;
```

## -description

The <b>TRUSTEE</b> structure identifies the user account, group account, or <a href="/windows/desktop/SecGloss/l-gly">logon session</a> to which an <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) applies. The structure can use a name or a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) to identify the trustee.

Access control functions, such as 
<a href="/windows/desktop/api/aclapi/nf-aclapi-setentriesinacla">SetEntriesInAcl</a> and 
<a href="/windows/desktop/api/aclapi/nf-aclapi-getexplicitentriesfromacla">GetExplicitEntriesFromAcl</a>, use this structure to identify the logon account associated with the access control or audit control information in an <a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structure.

## -struct-fields

### -field pMultipleTrustee

A pointer to a <b>TRUSTEE</b> structure that identifies a server account that can impersonate the user identified by the <b>ptstrName</b> member. This member is not currently supported and must be <b>NULL</b>.

### -field MultipleTrusteeOperation

A value of the 
<a href="/windows/desktop/api/accctrl/ne-accctrl-multiple_trustee_operation">MULTIPLE_TRUSTEE_OPERATION</a> enumeration type. Currently, this member must be NO_MULTIPLE_TRUSTEE.

### -field TrusteeForm

A value from the 
<a href="/windows/desktop/api/accctrl/ne-accctrl-trustee_form">TRUSTEE_FORM</a> enumeration type that indicates the type of data pointed to by the <b>ptstrName</b> member.
See <a href="#-remarks">Remarks</a> below.

### -field TrusteeType

A value from the 
<a href="/windows/desktop/api/accctrl/ne-accctrl-trustee_type">TRUSTEE_TYPE</a> enumeration type that indicates whether the trustee is a user account, a group account, or an unknown account type.

### -field ptstrName

A pointer whose form depends on the value of the <i>TrusteeForm</i> member, cast to LPCH.

<table>
<tr>
<th>TrusteeForm</th>
<th>Meaning of ptstrName</th>
</tr>
<tr>
<td width="40%"><a id="TRUSTEE_IS_NAME"></a><a id="trustee_is_name"></a><dl>
<dt><b>TRUSTEE_IS_NAME</b></dt>
</dl>
</td>
<td width="60%">
A pointer to a <b>null</b>-terminated string that contains the name of the trustee.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUSTEE_IS_OBJECTS_AND_NAME"></a><a id="trustee_is_objects_and_name"></a><dl>
<dt><b>TRUSTEE_IS_OBJECTS_AND_NAME</b></dt>
</dl>
</td>
<td width="60%">
A pointer to an 
<a href="/windows/desktop/api/accctrl/ns-accctrl-objects_and_name_a">OBJECTS_AND_NAME</a> structure that contains the name of the trustee and the names of the object types in an object-specific ACE.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUSTEE_IS_OBJECTS_AND_SID"></a><a id="trustee_is_objects_and_sid"></a><dl>
<dt><b>TRUSTEE_IS_OBJECTS_AND_SID</b></dt>
</dl>
</td>
<td width="60%">
A pointer to an 
<a href="/windows/desktop/api/accctrl/ns-accctrl-objects_and_sid">OBJECTS_AND_SID</a> structure that contains the SID of the trustee and the GUIDs of the object types in an object-specific ACE.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUSTEE_IS_SID"></a><a id="trustee_is_sid"></a><dl>
<dt><b>TRUSTEE_IS_SID</b></dt>
</dl>
</td>
<td width="60%">
A pointer to the SID of the trustee.
</td>
</tr>
</table>

## -remarks

A trustee name can have any of the following formats:

<ul>
<li>A fully qualified name, such as "g:\remotedir\abc".</li>
<li>A domain account, such as "domain1\xyz".</li>
<li>One of the predefined group names, such as "EVERYONE" or "GUEST".</li>
<li>One of the following special names. <table>
<tr>
<th>Name</th>
<th>Meaning</th>
</tr>
<tr>
<td>CREATOR GROUP</td>
<td>The CREATOR_GROUP SID is a SID used in inheritable ACEs. When a new object is created, the system replaces this SID with the primary group SID of the user who created the object.</td>
</tr>
<tr>
<td>CREATOR OWNER</td>
<td>The CREATOR_OWNER SID is a SID used in inheritable ACEs. When a new object is created, the system replaces this SID with the SID of the user who created the object.</td>
</tr>
<tr>
<td>CURRENT_USER</td>
<td>The owner of the calling thread or process.</td>
</tr>
</table>
 

</li>
</ul>
A trustee SID can be any user or group SID. It can also be any of the <a href="/windows/desktop/SecGloss/u-gly">universal, well-known SIDs</a>. For more information, see 
<a href="/windows/desktop/SecAuthZ/security-identifiers">Security Identifiers</a>.





> [!NOTE]
> The accctrl.h header defines TRUSTEE_ as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-getexplicitentriesfromacla">GetExplicitEntriesFromAcl</a>



<a href="/windows/desktop/api/accctrl/ne-accctrl-multiple_trustee_operation">MULTIPLE_TRUSTEE_OPERATION</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-objects_and_name_a">OBJECTS_AND_NAME</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-objects_and_sid">OBJECTS_AND_SID</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-setentriesinacla">SetEntriesInAcl</a>



<a href="/windows/desktop/api/accctrl/ne-accctrl-trustee_form">TRUSTEE_FORM</a>



<a href="/windows/desktop/api/accctrl/ne-accctrl-trustee_type">TRUSTEE_TYPE</a>
