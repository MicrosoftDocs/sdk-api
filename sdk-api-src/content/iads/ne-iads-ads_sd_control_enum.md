---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0048_0005
title: ADS_SD_CONTROL_ENUM (iads.h)
description: The ADS_SD_CONTROL_ENUM enumeration specifies control flags for a security descriptor.
helpviewer_keywords: ["ADS_SD_CONTROL_ENUM","ADS_SD_CONTROL_ENUM enumeration [ADSI]","ADS_SD_CONTROL_SE_DACL_AUTO_INHERITED","ADS_SD_CONTROL_SE_DACL_AUTO_INHERIT_REQ","ADS_SD_CONTROL_SE_DACL_DEFAULTED","ADS_SD_CONTROL_SE_DACL_PRESENT","ADS_SD_CONTROL_SE_DACL_PROTECTED","ADS_SD_CONTROL_SE_GROUP_DEFAULTED","ADS_SD_CONTROL_SE_OWNER_DEFAULTED","ADS_SD_CONTROL_SE_SACL_AUTO_INHERITED","ADS_SD_CONTROL_SE_SACL_AUTO_INHERIT_REQ","ADS_SD_CONTROL_SE_SACL_DEFAULTED","ADS_SD_CONTROL_SE_SACL_PRESENT","ADS_SD_CONTROL_SE_SACL_PROTECTED","ADS_SD_CONTROL_SE_SELF_RELATIVE","_ds_ads_sd_control_enum","adsi.ads__sd__control__enum","adsi.ads_sd_control_enum","iads/ADS_SD_CONTROL_ENUM","iads/ADS_SD_CONTROL_SE_DACL_AUTO_INHERITED","iads/ADS_SD_CONTROL_SE_DACL_AUTO_INHERIT_REQ","iads/ADS_SD_CONTROL_SE_DACL_DEFAULTED","iads/ADS_SD_CONTROL_SE_DACL_PRESENT","iads/ADS_SD_CONTROL_SE_DACL_PROTECTED","iads/ADS_SD_CONTROL_SE_GROUP_DEFAULTED","iads/ADS_SD_CONTROL_SE_OWNER_DEFAULTED","iads/ADS_SD_CONTROL_SE_SACL_AUTO_INHERITED","iads/ADS_SD_CONTROL_SE_SACL_AUTO_INHERIT_REQ","iads/ADS_SD_CONTROL_SE_SACL_DEFAULTED","iads/ADS_SD_CONTROL_SE_SACL_PRESENT","iads/ADS_SD_CONTROL_SE_SACL_PROTECTED","iads/ADS_SD_CONTROL_SE_SELF_RELATIVE"]
old-location: adsi\ads_sd_control_enum.htm
tech.root: adsi
ms.assetid: e34ddf53-c7c6-41b0-93e7-cf47152c77be
ms.date: 12/05/2018
ms.keywords: ADS_SD_CONTROL_ENUM, ADS_SD_CONTROL_ENUM enumeration [ADSI], ADS_SD_CONTROL_SE_DACL_AUTO_INHERITED, ADS_SD_CONTROL_SE_DACL_AUTO_INHERIT_REQ, ADS_SD_CONTROL_SE_DACL_DEFAULTED, ADS_SD_CONTROL_SE_DACL_PRESENT, ADS_SD_CONTROL_SE_DACL_PROTECTED, ADS_SD_CONTROL_SE_GROUP_DEFAULTED, ADS_SD_CONTROL_SE_OWNER_DEFAULTED, ADS_SD_CONTROL_SE_SACL_AUTO_INHERITED, ADS_SD_CONTROL_SE_SACL_AUTO_INHERIT_REQ, ADS_SD_CONTROL_SE_SACL_DEFAULTED, ADS_SD_CONTROL_SE_SACL_PRESENT, ADS_SD_CONTROL_SE_SACL_PROTECTED, ADS_SD_CONTROL_SE_SELF_RELATIVE, _ds_ads_sd_control_enum, adsi.ads__sd__control__enum, adsi.ads_sd_control_enum, iads/ADS_SD_CONTROL_ENUM, iads/ADS_SD_CONTROL_SE_DACL_AUTO_INHERITED, iads/ADS_SD_CONTROL_SE_DACL_AUTO_INHERIT_REQ, iads/ADS_SD_CONTROL_SE_DACL_DEFAULTED, iads/ADS_SD_CONTROL_SE_DACL_PRESENT, iads/ADS_SD_CONTROL_SE_DACL_PROTECTED, iads/ADS_SD_CONTROL_SE_GROUP_DEFAULTED, iads/ADS_SD_CONTROL_SE_OWNER_DEFAULTED, iads/ADS_SD_CONTROL_SE_SACL_AUTO_INHERITED, iads/ADS_SD_CONTROL_SE_SACL_AUTO_INHERIT_REQ, iads/ADS_SD_CONTROL_SE_SACL_DEFAULTED, iads/ADS_SD_CONTROL_SE_SACL_PRESENT, iads/ADS_SD_CONTROL_SE_SACL_PROTECTED, iads/ADS_SD_CONTROL_SE_SELF_RELATIVE
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
req.typenames: ADS_SD_CONTROL_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0001_0048_0005
 - iads/__MIDL___MIDL_itf_ads_0001_0048_0005
 - ADS_SD_CONTROL_ENUM
 - iads/ADS_SD_CONTROL_ENUM
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
 - ADS_SD_CONTROL_ENUM
---

# ADS_SD_CONTROL_ENUM enumeration


## -description

The <b>ADS_SD_CONTROL_ENUM</b> enumeration specifies control flags for a security descriptor.

## -enum-fields

### -field ADS_SD_CONTROL_SE_OWNER_DEFAULTED:0x1

A default mechanism provides the owner security identifier (SID) of the security descriptor rather than the original provider of the security descriptor.

### -field ADS_SD_CONTROL_SE_GROUP_DEFAULTED:0x2

A default mechanism provides the group SID of the security descriptor rather than the original provider of the security descriptor.

### -field ADS_SD_CONTROL_SE_DACL_PRESENT:0x4

The discretionary access-control list (DACL) is present in the security descriptor. If this flag is not set, or if this flag is set and the DACL is <b>NULL</b>, the security descriptor allows full access to everyone.

### -field ADS_SD_CONTROL_SE_DACL_DEFAULTED:0x8

The security descriptor uses a default DACL built from the creator's access token.

### -field ADS_SD_CONTROL_SE_SACL_PRESENT:0x10

The system access-control list (SACL) is present in the security descriptor.

### -field ADS_SD_CONTROL_SE_SACL_DEFAULTED:0x20

The security descriptor uses a default SACL built from the creator's access token.

### -field ADS_SD_CONTROL_SE_DACL_AUTO_INHERIT_REQ:0x100

THE DACL of the security descriptor must be inherited.

### -field ADS_SD_CONTROL_SE_SACL_AUTO_INHERIT_REQ:0x200

The SACL of the security descriptor must be inherited.

### -field ADS_SD_CONTROL_SE_DACL_AUTO_INHERITED:0x400

The DACL of the security descriptor supports automatic propagation of inheritable access-control entries (ACEs) to existing child objects.

### -field ADS_SD_CONTROL_SE_SACL_AUTO_INHERITED:0x800

The SACL of the security descriptor supports automatic propagation of inheritable ACEs to existing child objects.

### -field ADS_SD_CONTROL_SE_DACL_PROTECTED:0x1000

The security descriptor will not allow inheritable ACEs to modify the DACL.

### -field ADS_SD_CONTROL_SE_SACL_PROTECTED:0x2000

The security descriptor will not allow inheritable ACEs to modify the SACL.

### -field ADS_SD_CONTROL_SE_SELF_RELATIVE:0x8000

The security descriptor is of self-relative format with all the security information in a continuous block of memory.

## -remarks

For more information, see  <a href="/windows/desktop/SecAuthZ/access-control">Access Control</a> under Security in the Platform Software Development Kit (SDK).

Since VBScript cannot read information from a type library, VBScript applications do not understand the symbolic constants as defined above. You should use the numerical constants instead to set the appropriate flags in your VBScript applications. If you want to use the symbolic constants as a good programming practice, you should make explicit declarations of such constants, as done here, in your VBScript applications.

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI Enumerations</a>



<a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>
