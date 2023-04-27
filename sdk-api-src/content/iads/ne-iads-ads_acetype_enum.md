---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0048_0002
title: ADS_ACETYPE_ENUM (iads.h)
description: Used to specify the type of an access-control entry for Active Directory objects.
helpviewer_keywords: ["ADS_ACETYPE_ACCESS_ALLOWED","ADS_ACETYPE_ACCESS_ALLOWED_CALLBACK","ADS_ACETYPE_ACCESS_ALLOWED_CALLBACK_OBJECT","ADS_ACETYPE_ACCESS_ALLOWED_OBJECT","ADS_ACETYPE_ACCESS_DENIED","ADS_ACETYPE_ACCESS_DENIED_CALLBACK","ADS_ACETYPE_ACCESS_DENIED_CALLBACK_OBJECT","ADS_ACETYPE_ACCESS_DENIED_OBJECT","ADS_ACETYPE_ENUM","ADS_ACETYPE_ENUM enumeration [ADSI]","ADS_ACETYPE_SYSTEM_ALARM_CALLBACK","ADS_ACETYPE_SYSTEM_ALARM_CALLBACK_OBJECT","ADS_ACETYPE_SYSTEM_ALARM_OBJECT","ADS_ACETYPE_SYSTEM_AUDIT","ADS_ACETYPE_SYSTEM_AUDIT_CALLBACK","ADS_ACETYPE_SYSTEM_AUDIT_CALLBACK_OBJECT","ADS_ACETYPE_SYSTEM_AUDIT_OBJECT","_ds_ads_acetype_enum","adsi.ads__acetype__enum","adsi.ads_acetype_enum","iads/ADS_ACETYPE_ACCESS_ALLOWED","iads/ADS_ACETYPE_ACCESS_ALLOWED_CALLBACK","iads/ADS_ACETYPE_ACCESS_ALLOWED_CALLBACK_OBJECT","iads/ADS_ACETYPE_ACCESS_ALLOWED_OBJECT","iads/ADS_ACETYPE_ACCESS_DENIED","iads/ADS_ACETYPE_ACCESS_DENIED_CALLBACK","iads/ADS_ACETYPE_ACCESS_DENIED_CALLBACK_OBJECT","iads/ADS_ACETYPE_ACCESS_DENIED_OBJECT","iads/ADS_ACETYPE_ENUM","iads/ADS_ACETYPE_SYSTEM_ALARM_CALLBACK","iads/ADS_ACETYPE_SYSTEM_ALARM_CALLBACK_OBJECT","iads/ADS_ACETYPE_SYSTEM_ALARM_OBJECT","iads/ADS_ACETYPE_SYSTEM_AUDIT","iads/ADS_ACETYPE_SYSTEM_AUDIT_CALLBACK","iads/ADS_ACETYPE_SYSTEM_AUDIT_CALLBACK_OBJECT","iads/ADS_ACETYPE_SYSTEM_AUDIT_OBJECT"]
old-location: adsi\ads_acetype_enum.htm
tech.root: adsi
ms.assetid: dbdbf163-6c7b-4170-9a09-6ac45d808a79
ms.date: 12/05/2018
ms.keywords: ADS_ACETYPE_ACCESS_ALLOWED, ADS_ACETYPE_ACCESS_ALLOWED_CALLBACK, ADS_ACETYPE_ACCESS_ALLOWED_CALLBACK_OBJECT, ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, ADS_ACETYPE_ACCESS_DENIED, ADS_ACETYPE_ACCESS_DENIED_CALLBACK, ADS_ACETYPE_ACCESS_DENIED_CALLBACK_OBJECT, ADS_ACETYPE_ACCESS_DENIED_OBJECT, ADS_ACETYPE_ENUM, ADS_ACETYPE_ENUM enumeration [ADSI], ADS_ACETYPE_SYSTEM_ALARM_CALLBACK, ADS_ACETYPE_SYSTEM_ALARM_CALLBACK_OBJECT, ADS_ACETYPE_SYSTEM_ALARM_OBJECT, ADS_ACETYPE_SYSTEM_AUDIT, ADS_ACETYPE_SYSTEM_AUDIT_CALLBACK, ADS_ACETYPE_SYSTEM_AUDIT_CALLBACK_OBJECT, ADS_ACETYPE_SYSTEM_AUDIT_OBJECT, _ds_ads_acetype_enum, adsi.ads__acetype__enum, adsi.ads_acetype_enum, iads/ADS_ACETYPE_ACCESS_ALLOWED, iads/ADS_ACETYPE_ACCESS_ALLOWED_CALLBACK, iads/ADS_ACETYPE_ACCESS_ALLOWED_CALLBACK_OBJECT, iads/ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, iads/ADS_ACETYPE_ACCESS_DENIED, iads/ADS_ACETYPE_ACCESS_DENIED_CALLBACK, iads/ADS_ACETYPE_ACCESS_DENIED_CALLBACK_OBJECT, iads/ADS_ACETYPE_ACCESS_DENIED_OBJECT, iads/ADS_ACETYPE_ENUM, iads/ADS_ACETYPE_SYSTEM_ALARM_CALLBACK, iads/ADS_ACETYPE_SYSTEM_ALARM_CALLBACK_OBJECT, iads/ADS_ACETYPE_SYSTEM_ALARM_OBJECT, iads/ADS_ACETYPE_SYSTEM_AUDIT, iads/ADS_ACETYPE_SYSTEM_AUDIT_CALLBACK, iads/ADS_ACETYPE_SYSTEM_AUDIT_CALLBACK_OBJECT, iads/ADS_ACETYPE_SYSTEM_AUDIT_OBJECT
req.header: iads.h
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
req.typenames: ADS_ACETYPE_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0001_0048_0002
 - iads/__MIDL___MIDL_itf_ads_0001_0048_0002
 - ADS_ACETYPE_ENUM
 - iads/ADS_ACETYPE_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_ACETYPE_ENUM
---

# ADS_ACETYPE_ENUM enumeration


## -description

The <b>ADS_ACETYPE_ENUM</b> enumeration is used to specify the type of an access-control entry for Active Directory objects. The <a href="/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods">IADsAccessControlEntry.AceType</a> property contains one of these values for an Active Directory object.

For more information and possible values for file, file share and registry objects, see the <b>AceType</b> member of the <a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure.

## -enum-fields

### -field ADS_ACETYPE_ACCESS_ALLOWED:0

The ACE is of the standard ACCESS ALLOWED type, where the <b>ObjectType</b> and <b>InheritedObjectType</b> fields are <b>NULL</b>.

### -field ADS_ACETYPE_ACCESS_DENIED:0x1

The ACE is of the standard system-audit type, where the <b>ObjectType</b> and <b>InheritedObjectType</b> fields are <b>NULL</b>.

### -field ADS_ACETYPE_SYSTEM_AUDIT:0x2

The ACE is of the standard system type, where the <b>ObjectType</b> and <b>InheritedObjectType</b> fields are <b>NULL</b>.

### -field ADS_ACETYPE_ACCESS_ALLOWED_OBJECT:0x5

The ACE grants access to an object or a subobject of the object, such as a property set or property. <b>ObjectType</b> or <b>InheritedObjectType</b> or both contain a GUID that identifies a property set, property, extended right, or type of child object.

### -field ADS_ACETYPE_ACCESS_DENIED_OBJECT:0x6

The ACE denies access to an object or a subobject of the object, such as a property set or property. <b>ObjectType</b> or <b>InheritedObjectType</b> or both contain a GUID that identifies a property set, property, extended right, or type of child object.

### -field ADS_ACETYPE_SYSTEM_AUDIT_OBJECT:0x7

The ACE audits access to an object or a subobject of the object, such as a property set or property. <b>ObjectType</b> or <b>InheritedObjectType</b> or both contain a GUID that identifies a property set, property, extended right, or type of child object.

### -field ADS_ACETYPE_SYSTEM_ALARM_OBJECT:0x8

Not used.

### -field ADS_ACETYPE_ACCESS_ALLOWED_CALLBACK:0x9

Same functionality as <b>ADS_ACETYPE_ACCESS_ALLOWED</b>, but used with applications that use Authz to verify ACEs.

### -field ADS_ACETYPE_ACCESS_DENIED_CALLBACK:0xa

Same functionality as <b>ADS_ACETYPE_ACCESS_DENIED</b>, but used with applications that use Authz to verify ACEs.

### -field ADS_ACETYPE_ACCESS_ALLOWED_CALLBACK_OBJECT:0xb

Same functionality as <b>ADS_ACETYPE_ACCESS_ALLOWED_OBJECT</b>, but used with applications that use Authz to verify ACEs.

### -field ADS_ACETYPE_ACCESS_DENIED_CALLBACK_OBJECT:0xc

Same functionality as <b>ADS_ACETYPE_ACCESS_DENIED_OBJECT</b>, but used with applications that use Authz to check ACEs.

### -field ADS_ACETYPE_SYSTEM_AUDIT_CALLBACK:0xd

Same functionality as <b>ADS_ACETYPE_SYSTEM_AUDIT</b>, but used with applications that use Authz to check ACEs.

### -field ADS_ACETYPE_SYSTEM_ALARM_CALLBACK:0xe

Not used.

### -field ADS_ACETYPE_SYSTEM_AUDIT_CALLBACK_OBJECT:0xf

Same functionality as <b>ADS_ACETYPE_SYSTEM_AUDIT_OBJECT</b>, but used with applications that use Authz to verify ACEs.

### -field ADS_ACETYPE_SYSTEM_ALARM_CALLBACK_OBJECT:0x10

Not used.

## -remarks

A standard ACE is one defined and used in a Windows security descriptor. Windows enables the ACE to be applied to objects and properties identified by GUIDs.

Use the  <a href="/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry">IADsAccessControlEntry</a> property method to determine the ACE type.

<div class="alert"><b>Note</b>  Because Visual Basic Scripting Edition (VBScript) cannot read data from a type library, VBScript applications cannot recognize symbolic constants as defined above. Use the numeric constants instead to set the appropriate flags in VBScript applications. To use the symbolic constants as a good programming practice, write explicit declarations of such constants, as done here, in VBScript applications.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI Enumerations</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry">IADsAccessControlEntry</a>



<a href="/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods">IADsAccessControlEntry.AceType</a>
