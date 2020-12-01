---
UID: NS:winnt._ACE_HEADER
title: ACE_HEADER (winnt.h)
description: Defines the type and size of an access control entry (ACE).
helpviewer_keywords: ["*PACE_HEADER","ACCESS_ALLOWED_ACE_TYPE","ACCESS_ALLOWED_CALLBACK_ACE_TYPE","ACCESS_ALLOWED_CALLBACK_OBJECT_ACE_TYPE","ACCESS_ALLOWED_COMPOUND_ACE_TYPE","ACCESS_ALLOWED_OBJECT_ACE_TYPE","ACCESS_DENIED_ACE_TYPE","ACCESS_DENIED_CALLBACK_ACE_TYPE","ACCESS_DENIED_CALLBACK_OBJECT_ACE_TYPE","ACCESS_DENIED_OBJECT_ACE_TYPE","ACCESS_MAX_MS_ACE_TYPE","ACCESS_MAX_MS_OBJECT_ACE_TYPE","ACCESS_MAX_MS_V2_ACE_TYPE","ACCESS_MAX_MS_V3_ACE_TYPE","ACCESS_MAX_MS_V4_ACE_TYPE","ACCESS_MIN_MS_ACE_TYPE","ACCESS_MIN_MS_OBJECT_ACE_TYPE","ACE_HEADER","ACE_HEADER structure [Security]","CONTAINER_INHERIT_ACE","FAILED_ACCESS_ACE_FLAG","INHERITED_ACE","INHERIT_ONLY_ACE","NO_PROPAGATE_INHERIT_ACE","OBJECT_INHERIT_ACE","PACE_HEADER","PACE_HEADER structure pointer [Security]","SUCCESSFUL_ACCESS_ACE_FLAG","SYSTEM_ALARM_ACE_TYPE","SYSTEM_ALARM_CALLBACK_ACE_TYPE","SYSTEM_ALARM_CALLBACK_OBJECT_ACE_TYPE","SYSTEM_ALARM_OBJECT_ACE_TYPE","SYSTEM_AUDIT_ACE_TYPE","SYSTEM_AUDIT_CALLBACK_ACE_TYPE","SYSTEM_AUDIT_CALLBACK_OBJECT_ACE_TYPE","SYSTEM_AUDIT_OBJECT_ACE_TYPE","SYSTEM_MANDATORY_LABEL_ACE_TYPE","_ACE_HEADER","_win32_ace_header_str","security.ace_header","winnt/ACE_HEADER","winnt/PACE_HEADER"]
old-location: security\ace_header.htm
tech.root: security
ms.assetid: d23f15d6-0453-4aaf-a2db-7528b551a992
ms.date: 12/05/2018
ms.keywords: '*PACE_HEADER, ACCESS_ALLOWED_ACE_TYPE, ACCESS_ALLOWED_CALLBACK_ACE_TYPE, ACCESS_ALLOWED_CALLBACK_OBJECT_ACE_TYPE, ACCESS_ALLOWED_COMPOUND_ACE_TYPE, ACCESS_ALLOWED_OBJECT_ACE_TYPE, ACCESS_DENIED_ACE_TYPE, ACCESS_DENIED_CALLBACK_ACE_TYPE, ACCESS_DENIED_CALLBACK_OBJECT_ACE_TYPE, ACCESS_DENIED_OBJECT_ACE_TYPE, ACCESS_MAX_MS_ACE_TYPE, ACCESS_MAX_MS_OBJECT_ACE_TYPE, ACCESS_MAX_MS_V2_ACE_TYPE, ACCESS_MAX_MS_V3_ACE_TYPE, ACCESS_MAX_MS_V4_ACE_TYPE, ACCESS_MIN_MS_ACE_TYPE, ACCESS_MIN_MS_OBJECT_ACE_TYPE, ACE_HEADER, ACE_HEADER structure [Security], CONTAINER_INHERIT_ACE, FAILED_ACCESS_ACE_FLAG, INHERITED_ACE, INHERIT_ONLY_ACE, NO_PROPAGATE_INHERIT_ACE, OBJECT_INHERIT_ACE, PACE_HEADER, PACE_HEADER structure pointer [Security], SUCCESSFUL_ACCESS_ACE_FLAG, SYSTEM_ALARM_ACE_TYPE, SYSTEM_ALARM_CALLBACK_ACE_TYPE, SYSTEM_ALARM_CALLBACK_OBJECT_ACE_TYPE, SYSTEM_ALARM_OBJECT_ACE_TYPE, SYSTEM_AUDIT_ACE_TYPE, SYSTEM_AUDIT_CALLBACK_ACE_TYPE, SYSTEM_AUDIT_CALLBACK_OBJECT_ACE_TYPE, SYSTEM_AUDIT_OBJECT_ACE_TYPE, SYSTEM_MANDATORY_LABEL_ACE_TYPE, _ACE_HEADER, _win32_ace_header_str, security.ace_header, winnt/ACE_HEADER, winnt/PACE_HEADER'
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
req.typenames: ACE_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ACE_HEADER
 - winnt/_ACE_HEADER
 - ACE_HEADER
 - winnt/ACE_HEADER
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
 - ACE_HEADER
---

# ACE_HEADER structure


## -description

The <b>ACE_HEADER</b> structure defines the type and size of an <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE).

## -struct-fields

### -field AceType

Specifies the ACE type. This member can be one of the following values. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ACCESS_ALLOWED_ACE_TYPE"></a><a id="access_allowed_ace_type"></a><dl>
<dt><b>ACCESS_ALLOWED_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Access-allowed ACE that uses the 
<a href="/windows/desktop/api/winnt/ns-winnt-access_allowed_ace">ACCESS_ALLOWED_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_ALLOWED_CALLBACK_ACE_TYPE"></a><a id="access_allowed_callback_ace_type"></a><dl>
<dt><b>ACCESS_ALLOWED_CALLBACK_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Access-allowed callback ACE that uses the 
<a href="/windows/desktop/api/winnt/ns-winnt-access_allowed_callback_ace">ACCESS_ALLOWED_CALLBACK_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_ALLOWED_CALLBACK_OBJECT_ACE_TYPE"></a><a id="access_allowed_callback_object_ace_type"></a><dl>
<dt><b>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Object-specific access-allowed callback ACE that uses the 
<a href="/windows/desktop/api/winnt/ns-winnt-access_allowed_callback_object_ace">ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_ALLOWED_COMPOUND_ACE_TYPE"></a><a id="access_allowed_compound_ace_type"></a><dl>
<dt><b>ACCESS_ALLOWED_COMPOUND_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_ALLOWED_OBJECT_ACE_TYPE"></a><a id="access_allowed_object_ace_type"></a><dl>
<dt><b>ACCESS_ALLOWED_OBJECT_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Object-specific access-allowed ACE that uses the 
<a href="/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace">ACCESS_ALLOWED_OBJECT_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_DENIED_ACE_TYPE"></a><a id="access_denied_ace_type"></a><dl>
<dt><b>ACCESS_DENIED_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Access-denied ACE that uses the 
<a href="/windows/desktop/api/winnt/ns-winnt-access_denied_ace">ACCESS_DENIED_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_DENIED_CALLBACK_ACE_TYPE"></a><a id="access_denied_callback_ace_type"></a><dl>
<dt><b>ACCESS_DENIED_CALLBACK_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Access-denied callback ACE that uses the 
<a href="/windows/desktop/api/winnt/ns-winnt-access_denied_callback_ace">ACCESS_DENIED_CALLBACK_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_DENIED_CALLBACK_OBJECT_ACE_TYPE"></a><a id="access_denied_callback_object_ace_type"></a><dl>
<dt><b>ACCESS_DENIED_CALLBACK_OBJECT_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Object-specific access-denied callback ACE that uses the 
<a href="/windows/desktop/api/winnt/ns-winnt-access_denied_callback_ace">ACCESS_DENIED_CALLBACK_OBJECT_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_DENIED_OBJECT_ACE_TYPE"></a><a id="access_denied_object_ace_type"></a><dl>
<dt><b>ACCESS_DENIED_OBJECT_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Object-specific access-denied ACE that uses the 
<a href="/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace">ACCESS_DENIED_OBJECT_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_MAX_MS_ACE_TYPE"></a><a id="access_max_ms_ace_type"></a><dl>
<dt><b>ACCESS_MAX_MS_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Same as SYSTEM_ALARM_OBJECT_ACE_TYPE.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_MAX_MS_V2_ACE_TYPE"></a><a id="access_max_ms_v2_ace_type"></a><dl>
<dt><b>ACCESS_MAX_MS_V2_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Same as SYSTEM_ALARM_ACE_TYPE.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_MAX_MS_V3_ACE_TYPE"></a><a id="access_max_ms_v3_ace_type"></a><dl>
<dt><b>ACCESS_MAX_MS_V3_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_MAX_MS_V4_ACE_TYPE"></a><a id="access_max_ms_v4_ace_type"></a><dl>
<dt><b>ACCESS_MAX_MS_V4_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Same as SYSTEM_ALARM_OBJECT_ACE_TYPE.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_MAX_MS_OBJECT_ACE_TYPE"></a><a id="access_max_ms_object_ace_type"></a><dl>
<dt><b>ACCESS_MAX_MS_OBJECT_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Same as SYSTEM_ALARM_OBJECT_ACE_TYPE.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_MIN_MS_ACE_TYPE"></a><a id="access_min_ms_ace_type"></a><dl>
<dt><b>ACCESS_MIN_MS_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Same as ACCESS_ALLOWED_ACE_TYPE.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_MIN_MS_OBJECT_ACE_TYPE"></a><a id="access_min_ms_object_ace_type"></a><dl>
<dt><b>ACCESS_MIN_MS_OBJECT_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Same as ACCESS_ALLOWED_OBJECT_ACE_TYPE.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_ALARM_ACE_TYPE"></a><a id="system_alarm_ace_type"></a><dl>
<dt><b>SYSTEM_ALARM_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Reserved for future use. System-alarm ACE that uses the <a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_ace">SYSTEM_ALARM_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_ALARM_CALLBACK_ACE_TYPE"></a><a id="system_alarm_callback_ace_type"></a><dl>
<dt><b>SYSTEM_ALARM_CALLBACK_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Reserved for future use. System-alarm callback ACE that uses the <a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_callback_ace">SYSTEM_ALARM_CALLBACK_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_ALARM_CALLBACK_OBJECT_ACE_TYPE"></a><a id="system_alarm_callback_object_ace_type"></a><dl>
<dt><b>SYSTEM_ALARM_CALLBACK_OBJECT_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Reserved for future use. Object-specific system-alarm callback ACE that uses the <a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_callback_object_ace">SYSTEM_ALARM_CALLBACK_OBJECT_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_ALARM_OBJECT_ACE_TYPE"></a><a id="system_alarm_object_ace_type"></a><dl>
<dt><b>SYSTEM_ALARM_OBJECT_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Reserved for future use. Object-specific system-alarm ACE that uses the <a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace">SYSTEM_ALARM_OBJECT_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_AUDIT_ACE_TYPE"></a><a id="system_audit_ace_type"></a><dl>
<dt><b>SYSTEM_AUDIT_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
System-audit ACE that uses the 
<a href="/windows/desktop/api/winnt/ns-winnt-system_audit_ace">SYSTEM_AUDIT_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_AUDIT_CALLBACK_ACE_TYPE"></a><a id="system_audit_callback_ace_type"></a><dl>
<dt><b>SYSTEM_AUDIT_CALLBACK_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
System-audit callback ACE that uses the 
<a href="/windows/desktop/api/winnt/ns-winnt-system_audit_callback_ace">SYSTEM_AUDIT_CALLBACK_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_AUDIT_CALLBACK_OBJECT_ACE_TYPE"></a><a id="system_audit_callback_object_ace_type"></a><dl>
<dt><b>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Object-specific system-audit callback ACE that uses the 
<a href="/windows/desktop/api/winnt/ns-winnt-system_audit_callback_object_ace">SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_AUDIT_OBJECT_ACE_TYPE"></a><a id="system_audit_object_ace_type"></a><dl>
<dt><b>SYSTEM_AUDIT_OBJECT_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Object-specific system-audit ACE that uses the 
<a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace">SYSTEM_AUDIT_OBJECT_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_MANDATORY_LABEL_ACE_TYPE"></a><a id="system_mandatory_label_ace_type"></a><dl>
<dt><b>SYSTEM_MANDATORY_LABEL_ACE_TYPE</b></dt>
<dt>0x11</dt>
</dl>
</td>
<td width="60%">
Mandatory label ACE that uses the <a href="/windows/desktop/api/winnt/ns-winnt-system_mandatory_label_ace">SYSTEM_MANDATORY_LABEL_ACE</a> structure.

</td>
</tr>
</table>

### -field AceFlags

Specifies a set of ACE type-specific control flags. This member can be a combination of the following values. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CONTAINER_INHERIT_ACE"></a><a id="container_inherit_ace"></a><dl>
<dt><b>CONTAINER_INHERIT_ACE</b></dt>
</dl>
</td>
<td width="60%">
Child objects that are containers, such as directories, inherit the ACE as an effective ACE. The inherited ACE is inheritable unless the NO_PROPAGATE_INHERIT_ACE bit flag is also set.

</td>
</tr>
<tr>
<td width="40%"><a id="FAILED_ACCESS_ACE_FLAG"></a><a id="failed_access_ace_flag"></a><dl>
<dt><b>FAILED_ACCESS_ACE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Used with system-audit ACEs in a <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) to generate audit messages for failed access attempts.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERIT_ONLY_ACE"></a><a id="inherit_only_ace"></a><dl>
<dt><b>INHERIT_ONLY_ACE</b></dt>
</dl>
</td>
<td width="60%">
Indicates an inherit-only ACE, which does not control access to the object to which it is attached. If this flag is not set, the ACE is an effective ACE which controls access to the object to which it is attached. 




Both effective and inherit-only ACEs can be inherited depending on the state of the other inheritance flags.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERITED_ACE"></a><a id="inherited_ace"></a><dl>
<dt><b>INHERITED_ACE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the ACE was inherited. The system sets this bit when it propagates an inherited ACE to a child object.

</td>
</tr>
<tr>
<td width="40%"><a id="NO_PROPAGATE_INHERIT_ACE"></a><a id="no_propagate_inherit_ace"></a><dl>
<dt><b>NO_PROPAGATE_INHERIT_ACE</b></dt>
</dl>
</td>
<td width="60%">
If the ACE is inherited by a child object, the system clears the OBJECT_INHERIT_ACE and CONTAINER_INHERIT_ACE flags in the inherited ACE. This prevents the ACE from being inherited by subsequent generations of objects.

</td>
</tr>
<tr>
<td width="40%"><a id="OBJECT_INHERIT_ACE"></a><a id="object_inherit_ace"></a><dl>
<dt><b>OBJECT_INHERIT_ACE</b></dt>
</dl>
</td>
<td width="60%">
Noncontainer child objects inherit the ACE as an effective ACE. 




For child objects that are containers, the ACE is inherited as an inherit-only ACE unless the NO_PROPAGATE_INHERIT_ACE bit flag is also set.

</td>
</tr>
<tr>
<td width="40%"><a id="SUCCESSFUL_ACCESS_ACE_FLAG"></a><a id="successful_access_ace_flag"></a><dl>
<dt><b>SUCCESSFUL_ACCESS_ACE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Used with system-audit ACEs in a SACL to generate audit messages for successful access attempts.

</td>
</tr>
</table>

### -field AceSize

Specifies the size, in bytes, of the ACE.

## -remarks

The <b>ACE_HEADER</b> structure is the first member of the various types of ACE structures, such as <a href="/windows/desktop/api/winnt/ns-winnt-access_allowed_ace">ACCESS_ALLOWED_ACE</a>.

System-alarm ACEs are not currently supported. The <b>AceType</b> member cannot specify the SYSTEM_ALARM_ACE_TYPE or SYSTEM_ALARM_OBJECT_ACE_TYPE values. Do not use the <a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_ace">SYSTEM_ALARM_ACE</a> or <a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace">SYSTEM_ALARM_OBJECT_ACE</a> structures.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-access_allowed_ace">ACCESS_ALLOWED_ACE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace">ACCESS_ALLOWED_OBJECT_ACE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-access_denied_ace">ACCESS_DENIED_ACE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace">ACCESS_DENIED_OBJECT_ACE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/api/winnt/ns-winnt-system_audit_ace">SYSTEM_AUDIT_ACE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace">SYSTEM_AUDIT_OBJECT_ACE</a>