---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0048_0003
title: ADS_ACEFLAG_ENUM (iads.h)
description: The ADS_ACEFLAG_ENUM enumeration is used to specify the behavior of an Access Control Entry (ACE) for an Active Directory object.
helpviewer_keywords: ["ADS_ACEFLAG_ENUM","ADS_ACEFLAG_ENUM enumeration [ADSI]","ADS_ACEFLAG_FAILED_ACCESS","ADS_ACEFLAG_INHERITED_ACE","ADS_ACEFLAG_INHERIT_ACE","ADS_ACEFLAG_INHERIT_ONLY_ACE","ADS_ACEFLAG_NO_PROPAGATE_INHERIT_ACE","ADS_ACEFLAG_SUCCESSFUL_ACCESS","ADS_ACEFLAG_VALID_INHERIT_FLAGS","_ds_ads_aceflag_enum","adsi.ads__aceflag__enum","adsi.ads_aceflag_enum","iads/ADS_ACEFLAG_ENUM","iads/ADS_ACEFLAG_FAILED_ACCESS","iads/ADS_ACEFLAG_INHERITED_ACE","iads/ADS_ACEFLAG_INHERIT_ACE","iads/ADS_ACEFLAG_INHERIT_ONLY_ACE","iads/ADS_ACEFLAG_NO_PROPAGATE_INHERIT_ACE","iads/ADS_ACEFLAG_SUCCESSFUL_ACCESS","iads/ADS_ACEFLAG_VALID_INHERIT_FLAGS"]
old-location: adsi\ads_aceflag_enum.htm
tech.root: adsi
ms.assetid: 4fd63de4-b699-420b-96f9-28f86d3aca01
ms.date: 12/05/2018
ms.keywords: ADS_ACEFLAG_ENUM, ADS_ACEFLAG_ENUM enumeration [ADSI], ADS_ACEFLAG_FAILED_ACCESS, ADS_ACEFLAG_INHERITED_ACE, ADS_ACEFLAG_INHERIT_ACE, ADS_ACEFLAG_INHERIT_ONLY_ACE, ADS_ACEFLAG_NO_PROPAGATE_INHERIT_ACE, ADS_ACEFLAG_SUCCESSFUL_ACCESS, ADS_ACEFLAG_VALID_INHERIT_FLAGS, _ds_ads_aceflag_enum, adsi.ads__aceflag__enum, adsi.ads_aceflag_enum, iads/ADS_ACEFLAG_ENUM, iads/ADS_ACEFLAG_FAILED_ACCESS, iads/ADS_ACEFLAG_INHERITED_ACE, iads/ADS_ACEFLAG_INHERIT_ACE, iads/ADS_ACEFLAG_INHERIT_ONLY_ACE, iads/ADS_ACEFLAG_NO_PROPAGATE_INHERIT_ACE, iads/ADS_ACEFLAG_SUCCESSFUL_ACCESS, iads/ADS_ACEFLAG_VALID_INHERIT_FLAGS
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
req.typenames: ADS_ACEFLAG_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0001_0048_0003
 - iads/__MIDL___MIDL_itf_ads_0001_0048_0003
 - ADS_ACEFLAG_ENUM
 - iads/ADS_ACEFLAG_ENUM
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
 - ADS_ACEFLAG_ENUM
---

# ADS_ACEFLAG_ENUM enumeration


## -description

The <b>ADS_ACEFLAG_ENUM</b> enumeration is used to specify the behavior of an Access Control Entry (ACE) for an Active Directory object.

For more information and possible values for file, file share and registry objects, see the <b>AceFlags</b> member of the <a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure.

## -enum-fields

### -field ADS_ACEFLAG_INHERIT_ACE:0x2

Child objects will inherit this access-control entry (ACE). The inherited ACE is inheritable unless the ADS_ACEFLAG_NO_PROPAGATE_INHERIT_ACE flag is set.

### -field ADS_ACEFLAG_NO_PROPAGATE_INHERIT_ACE:0x4

The system will clear the ADS_ACEFLAG_INHERIT_ACE flag for the inherited ACEs of child objects. This prevents the ACE from being inherited by subsequent generations of objects.

### -field ADS_ACEFLAG_INHERIT_ONLY_ACE:0x8

Indicates that an inherit-only ACE that does not exercise access control on the object to which it is attached. If this flag is not set, the ACE is an effective ACE that exerts access control on the object to which it is attached.

### -field ADS_ACEFLAG_INHERITED_ACE:0x10

Indicates whether or not the ACE was inherited. The system sets this bit.

### -field ADS_ACEFLAG_VALID_INHERIT_FLAGS:0x1f

Indicates whether the inherit flags are valid. The system sets this bit.

### -field ADS_ACEFLAG_SUCCESSFUL_ACCESS:0x40

Generates audit messages for successful access attempts, used with ACEs that audit the system in a system access-control list (SACL).

### -field ADS_ACEFLAG_FAILED_ACCESS:0x80

Generates audit messages for failed access attempts, used with ACEs that audit the system in a SACL.

## -remarks

Because VBScript cannot read data from a type library, VBScript applications do not understand the symbolic constants as defined in these enumerations. You should use the numerical constants instead to set the appropriate flags in your VBScript applications. If you want to use the symbolic constants as a good programming practice, write explicit declarations of such constants, as done here, in your VBScript applications.

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI Enumerations</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsobjectoptions">IADsObjectOptions</a>



<a href="/windows/desktop/api/iads/nf-iads-iadspathname-set">IADsPathname::Set</a>
