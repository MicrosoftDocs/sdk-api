---
UID: NS:winnt._SYSTEM_ALARM_CALLBACK_OBJECT_ACE
title: "_SYSTEM_ALARM_CALLBACK_OBJECT_ACE"
author: windows-sdk-content
description: The SYSTEM_ALARM_CALLBACK_OBJECT_ACE structure is reserved for future use.
old-location: security\system_alarm_callback_object_ace.htm
old-project: SecAuthZ
ms.assetid: 3fdd0b75-666a-4064-95ed-9e708f34bed6
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*PSYSTEM_ALARM_CALLBACK_OBJECT_ACE, ACE_INHERITED_OBJECT_TYPE_PRESENT, ACE_OBJECT_TYPE_PRESENT, ADS_RIGHT_DS_CONTROL_ACCESS, ADS_RIGHT_DS_CREATE_CHILD, ADS_RIGHT_DS_READ_PROP and/or ADS_RIGHT_DS_WRITE_PROP, ADS_RIGHT_DS_SELF, SYSTEM_ALARM_CALLBACK_OBJECT_ACE, SYSTEM_ALARM_CALLBACK_OBJECT_ACE structure [Security], _SYSTEM_ALARM_CALLBACK_OBJECT_ACE, security.system_alarm_callback_object_ace, winnt/SYSTEM_ALARM_CALLBACK_OBJECT_ACE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: 
req.target-type: Windows
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
req.typenames: SYSTEM_ALARM_CALLBACK_OBJECT_ACE, *PSYSTEM_ALARM_CALLBACK_OBJECT_ACE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winnt.h
api_name:
-	SYSTEM_ALARM_CALLBACK_OBJECT_ACE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _SYSTEM_ALARM_CALLBACK_OBJECT_ACE structure


## -description


Not supported.

The <b>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</b> structure is reserved for future use.


## -struct-fields




### -field Header


<a href="https://msdn.microsoft.com/library/windows/hardware/ff538847">ACE_HEADER</a> structure that specifies the size and type of ACE. It contains flags that control inheritance of the ACE by child objects. The structure also contains flags that indicate whether the ACE audits successful access attempts, failed access attempts, or both. The <b>AceType</b> member of the <b>ACE_HEADER</b> structure should be set to SYSTEM_ALARM_CALLBACK_OBJECT_ACE_TYPE.


### -field Mask

An 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a> that specifies the access rights the system will audit for access attempts by the <a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">trustee</a>.


### -field Flags

A set of bit flags that indicate whether the <b>ObjectType</b> and <b>InheritedObjectType</b> members contain GUIDs. This parameter can be a combination of the following values. Set all undefined bits to zero. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ACE_OBJECT_TYPE_PRESENT"></a><a id="ace_object_type_present"></a><dl>
<dt><b>ACE_OBJECT_TYPE_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The <b>ObjectType</b> member contains a GUID.

</td>
</tr>
<tr>
<td width="40%"><a id="ACE_INHERITED_OBJECT_TYPE_PRESENT"></a><a id="ace_inherited_object_type_present"></a><dl>
<dt><b>ACE_INHERITED_OBJECT_TYPE_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The <b>InheritedObjectType</b> member contains a GUID.

</td>
</tr>
</table>
 


### -field ObjectType

A 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a> structure that identifies a property set, property, extended right, or type of child object. 




This member is valid only if the ACE_OBJECT_TYPE_PRESENT bit is set in the <b>Flags</b> member. Otherwise, <b>ObjectType</b> is ignored.

The purpose of this GUID depends on the access rights specified in the <b>Mask</b> member.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ADS_RIGHT_DS_READ_PROP_and_or_ADS_RIGHT_DS_WRITE_PROP"></a><a id="ads_right_ds_read_prop_and_or_ads_right_ds_write_prop"></a><a id="ADS_RIGHT_DS_READ_PROP_AND_OR_ADS_RIGHT_DS_WRITE_PROP"></a><dl>
<dt><b>ADS_RIGHT_DS_READ_PROP and/or ADS_RIGHT_DS_WRITE_PROP</b></dt>
</dl>
</td>
<td width="60%">
The <b>ObjectType</b> GUID identifies a property set or property of the object. The ACE controls auditing of the trustee's attempts to read or write the property or property set.

</td>
</tr>
<tr>
<td width="40%"><a id="ADS_RIGHT_DS_CONTROL_ACCESS"></a><a id="ads_right_ds_control_access"></a><dl>
<dt><b>ADS_RIGHT_DS_CONTROL_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
The <b>ObjectType</b> GUID identifies an extended access right.

</td>
</tr>
<tr>
<td width="40%"><a id="ADS_RIGHT_DS_CREATE_CHILD"></a><a id="ads_right_ds_create_child"></a><dl>
<dt><b>ADS_RIGHT_DS_CREATE_CHILD</b></dt>
</dl>
</td>
<td width="60%">
The <b>ObjectType</b> GUID identifies a type of child object. The ACE controls auditing of the trustee's attempts to create this type of child object.

</td>
</tr>
<tr>
<td width="40%"><a id="ADS_RIGHT_DS_SELF"></a><a id="ads_right_ds_self"></a><dl>
<dt><b>ADS_RIGHT_DS_SELF</b></dt>
</dl>
</td>
<td width="60%">
The <b>ObjectType</b> GUID identifies a validated write.

</td>
</tr>
</table>
 


### -field InheritedObjectType

A <a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a> structure that identifies the type of child object that can inherit the ACE. 




This member is valid only if the ACE_INHERITED_OBJECT_TYPE_PRESENT bit is set in the <b>Flags</b> member. If that bit is not set, <b>InheritedObjectType</b> is ignored and all types of child objects can inherit the ACE. In either case, inheritance is also controlled by the inheritance flags in the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff538847">ACE_HEADER</a>, as well as by any protection against inheritance placed on the child objects.


### -field SidStart

The first <b>DWORD</b> of a trustee's ACE. This ACE can be appended with application data. When the <a href="https://msdn.microsoft.com/e8a510e6-0739-4765-ad07-3bcb1b9c905c">AuthzAccessCheckCallback</a> function is called, this ACE is passed as the <i>pAce</i> parameter of that function.


## -remarks



If neither the <b>ObjectType</b> nor <b>InheritedObjectType</b> GUID is specified, the <b>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</b> structure has the same semantics as the <a href="https://msdn.microsoft.com/8bfb579f-4bee-454e-827b-63a800bccf85">SYSTEM_ALARM_CALLBACK_ACE</a> structure. In that case, use the 
<b>SYSTEM_ALARM_CALLBACK_ACE</b> structure because it is smaller and more efficient.

An ACL that contains an <b>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</b> must specify the ACL_REVISION_DS revision number in its 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff538847">ACE_HEADER</a> structure.



