---
UID: NS:winnt._ACE_HEADER
title: "_ACE_HEADER"
author: windows-sdk-content
description: Defines the type and size of an access control entry (ACE).
old-location: security\ace_header.htm
old-project: secauthz
ms.assetid: d23f15d6-0453-4aaf-a2db-7528b551a992
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: "*PACE_HEADER, ACCESS_ALLOWED_ACE_TYPE, ACCESS_ALLOWED_CALLBACK_ACE_TYPE, ACCESS_ALLOWED_CALLBACK_OBJECT_ACE_TYPE, ACCESS_ALLOWED_COMPOUND_ACE_TYPE, ACCESS_ALLOWED_OBJECT_ACE_TYPE, ACCESS_DENIED_ACE_TYPE, ACCESS_DENIED_CALLBACK_ACE_TYPE, ACCESS_DENIED_CALLBACK_OBJECT_ACE_TYPE, ACCESS_DENIED_OBJECT_ACE_TYPE, ACCESS_MAX_MS_ACE_TYPE, ACCESS_MAX_MS_OBJECT_ACE_TYPE, ACCESS_MAX_MS_V2_ACE_TYPE, ACCESS_MAX_MS_V3_ACE_TYPE, ACCESS_MAX_MS_V4_ACE_TYPE, ACCESS_MIN_MS_ACE_TYPE, ACCESS_MIN_MS_OBJECT_ACE_TYPE, ACE_HEADER, ACE_HEADER structure [Security], CONTAINER_INHERIT_ACE, FAILED_ACCESS_ACE_FLAG, INHERITED_ACE, INHERIT_ONLY_ACE, NO_PROPAGATE_INHERIT_ACE, OBJECT_INHERIT_ACE, PACE_HEADER, PACE_HEADER structure pointer [Security], SUCCESSFUL_ACCESS_ACE_FLAG, SYSTEM_ALARM_ACE_TYPE, SYSTEM_ALARM_CALLBACK_ACE_TYPE, SYSTEM_ALARM_CALLBACK_OBJECT_ACE_TYPE, SYSTEM_ALARM_OBJECT_ACE_TYPE, SYSTEM_AUDIT_ACE_TYPE, SYSTEM_AUDIT_CALLBACK_ACE_TYPE, SYSTEM_AUDIT_CALLBACK_OBJECT_ACE_TYPE, SYSTEM_AUDIT_OBJECT_ACE_TYPE, SYSTEM_MANDATORY_LABEL_ACE_TYPE, _ACE_HEADER, _win32_ace_header_str, security.ace_header, winnt/ACE_HEADER, winnt/PACE_HEADER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: ACE_HEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - ACE_HEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _ACE_HEADER structure


## -description


The <b>ACE_HEADER</b> structure defines the type and size of an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE).


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
<a href="https://msdn.microsoft.com/002a3fa7-02a3-4832-948e-b048f5f5818f">ACCESS_ALLOWED_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_ALLOWED_CALLBACK_ACE_TYPE"></a><a id="access_allowed_callback_ace_type"></a><dl>
<dt><b>ACCESS_ALLOWED_CALLBACK_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Access-allowed callback ACE that uses the 
<a href="https://msdn.microsoft.com/0dbca19b-4b54-4c55-920a-c00335692d68">ACCESS_ALLOWED_CALLBACK_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_ALLOWED_CALLBACK_OBJECT_ACE_TYPE"></a><a id="access_allowed_callback_object_ace_type"></a><dl>
<dt><b>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Object-specific access-allowed callback ACE that uses the 
<a href="https://msdn.microsoft.com/83b00ef3-f7b2-455e-8f3f-01b1da6024b7">ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</a> structure.

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
<a href="https://msdn.microsoft.com/ee91ca50-e81b-4872-95eb-349c2d5be004">ACCESS_ALLOWED_OBJECT_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_DENIED_ACE_TYPE"></a><a id="access_denied_ace_type"></a><dl>
<dt><b>ACCESS_DENIED_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Access-denied ACE that uses the 
<a href="https://msdn.microsoft.com/d76a92d0-ccd0-4e73-98b6-43bcd661134d">ACCESS_DENIED_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_DENIED_CALLBACK_ACE_TYPE"></a><a id="access_denied_callback_ace_type"></a><dl>
<dt><b>ACCESS_DENIED_CALLBACK_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Access-denied callback ACE that uses the 
<a href="https://msdn.microsoft.com/6df77b27-7aa3-455f-bffe-eeb90ba1bc15">ACCESS_DENIED_CALLBACK_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_DENIED_CALLBACK_OBJECT_ACE_TYPE"></a><a id="access_denied_callback_object_ace_type"></a><dl>
<dt><b>ACCESS_DENIED_CALLBACK_OBJECT_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Object-specific access-denied callback ACE that uses the 
<a href="https://msdn.microsoft.com/6df77b27-7aa3-455f-bffe-eeb90ba1bc15">ACCESS_DENIED_CALLBACK_OBJECT_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_DENIED_OBJECT_ACE_TYPE"></a><a id="access_denied_object_ace_type"></a><dl>
<dt><b>ACCESS_DENIED_OBJECT_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Object-specific access-denied ACE that uses the 
<a href="https://msdn.microsoft.com/80e00c2b-7c31-428d-96c1-c4e3d22619f3">ACCESS_DENIED_OBJECT_ACE</a> structure.

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
Reserved for future use. System-alarm ACE that uses the <a href="https://msdn.microsoft.com/491cc5c7-abb6-4d03-b3b0-ba5eedb5e2ba">SYSTEM_ALARM_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_ALARM_CALLBACK_ACE_TYPE"></a><a id="system_alarm_callback_ace_type"></a><dl>
<dt><b>SYSTEM_ALARM_CALLBACK_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Reserved for future use. System-alarm callback ACE that uses the <a href="https://msdn.microsoft.com/8bfb579f-4bee-454e-827b-63a800bccf85">SYSTEM_ALARM_CALLBACK_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_ALARM_CALLBACK_OBJECT_ACE_TYPE"></a><a id="system_alarm_callback_object_ace_type"></a><dl>
<dt><b>SYSTEM_ALARM_CALLBACK_OBJECT_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Reserved for future use. Object-specific system-alarm callback ACE that uses the <a href="https://msdn.microsoft.com/3fdd0b75-666a-4064-95ed-9e708f34bed6">SYSTEM_ALARM_CALLBACK_OBJECT_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_ALARM_OBJECT_ACE_TYPE"></a><a id="system_alarm_object_ace_type"></a><dl>
<dt><b>SYSTEM_ALARM_OBJECT_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Reserved for future use. Object-specific system-alarm ACE that uses the <a href="https://msdn.microsoft.com/a55f6039-d1d2-4a7d-a6c9-e8f51b291582">SYSTEM_ALARM_OBJECT_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_AUDIT_ACE_TYPE"></a><a id="system_audit_ace_type"></a><dl>
<dt><b>SYSTEM_AUDIT_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
System-audit ACE that uses the 
<a href="https://msdn.microsoft.com/c26b5856-5447-4606-8110-f24a4d235c64">SYSTEM_AUDIT_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_AUDIT_CALLBACK_ACE_TYPE"></a><a id="system_audit_callback_ace_type"></a><dl>
<dt><b>SYSTEM_AUDIT_CALLBACK_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
System-audit callback ACE that uses the 
<a href="https://msdn.microsoft.com/4d1799b0-3e55-48d7-94ff-c0094945adea">SYSTEM_AUDIT_CALLBACK_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_AUDIT_CALLBACK_OBJECT_ACE_TYPE"></a><a id="system_audit_callback_object_ace_type"></a><dl>
<dt><b>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Object-specific system-audit callback ACE that uses the 
<a href="https://msdn.microsoft.com/f547c928-4850-4072-be05-76a6c83b79bb">SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_AUDIT_OBJECT_ACE_TYPE"></a><a id="system_audit_object_ace_type"></a><dl>
<dt><b>SYSTEM_AUDIT_OBJECT_ACE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Object-specific system-audit ACE that uses the 
<a href="https://msdn.microsoft.com/de37bef6-e6c8-4455-856a-adebebda4cc7">SYSTEM_AUDIT_OBJECT_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_MANDATORY_LABEL_ACE_TYPE"></a><a id="system_mandatory_label_ace_type"></a><dl>
<dt><b>SYSTEM_MANDATORY_LABEL_ACE_TYPE</b></dt>
<dt>0x11</dt>
</dl>
</td>
<td width="60%">
Mandatory label ACE that uses the <a href="https://msdn.microsoft.com/77b7716c-b445-4473-a2e3-4a78f9fbebe3">SYSTEM_MANDATORY_LABEL_ACE</a> structure.

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
Used with system-audit ACEs in a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) to generate audit messages for failed access attempts.

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



The <b>ACE_HEADER</b> structure is the first member of the various types of ACE structures, such as <a href="https://msdn.microsoft.com/002a3fa7-02a3-4832-948e-b048f5f5818f">ACCESS_ALLOWED_ACE</a>.

System-alarm ACEs are not currently supported. The <b>AceType</b> member cannot specify the SYSTEM_ALARM_ACE_TYPE or SYSTEM_ALARM_OBJECT_ACE_TYPE values. Do not use the <a href="https://msdn.microsoft.com/491cc5c7-abb6-4d03-b3b0-ba5eedb5e2ba">SYSTEM_ALARM_ACE</a> or <a href="https://msdn.microsoft.com/a55f6039-d1d2-4a7d-a6c9-e8f51b291582">SYSTEM_ALARM_OBJECT_ACE</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/002a3fa7-02a3-4832-948e-b048f5f5818f">ACCESS_ALLOWED_ACE</a>



<a href="https://msdn.microsoft.com/ee91ca50-e81b-4872-95eb-349c2d5be004">ACCESS_ALLOWED_OBJECT_ACE</a>



<a href="https://msdn.microsoft.com/d76a92d0-ccd0-4e73-98b6-43bcd661134d">ACCESS_DENIED_ACE</a>



<a href="https://msdn.microsoft.com/80e00c2b-7c31-428d-96c1-c4e3d22619f3">ACCESS_DENIED_OBJECT_ACE</a>



<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a>



<a href="https://msdn.microsoft.com/c26b5856-5447-4606-8110-f24a4d235c64">SYSTEM_AUDIT_ACE</a>



<a href="https://msdn.microsoft.com/de37bef6-e6c8-4455-856a-adebebda4cc7">SYSTEM_AUDIT_OBJECT_ACE</a>
 

 

