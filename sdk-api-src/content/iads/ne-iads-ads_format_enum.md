---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0078_0002
title: ADS_FORMAT_ENUM (iads.h)
description: Specifies the available path value types used by the IADsPathname::Retrieve method.
helpviewer_keywords: ["ADS_FORMAT_ENUM","ADS_FORMAT_ENUM enumeration [ADSI]","ADS_FORMAT_LEAF","ADS_FORMAT_PROVIDER","ADS_FORMAT_SERVER","ADS_FORMAT_WINDOWS","ADS_FORMAT_WINDOWS_DN","ADS_FORMAT_WINDOWS_NO_SERVER","ADS_FORMAT_WINDOWS_PARENT","ADS_FORMAT_X500","ADS_FORMAT_X500_DN","ADS_FORMAT_X500_NO_SERVER","ADS_FORMAT_X500_PARENT","_ds_ads_format_enum","adsi.ads__format__enum","adsi.ads_format_enum","iads/ADS_FORMAT_ENUM","iads/ADS_FORMAT_LEAF","iads/ADS_FORMAT_PROVIDER","iads/ADS_FORMAT_SERVER","iads/ADS_FORMAT_WINDOWS","iads/ADS_FORMAT_WINDOWS_DN","iads/ADS_FORMAT_WINDOWS_NO_SERVER","iads/ADS_FORMAT_WINDOWS_PARENT","iads/ADS_FORMAT_X500","iads/ADS_FORMAT_X500_DN","iads/ADS_FORMAT_X500_NO_SERVER","iads/ADS_FORMAT_X500_PARENT"]
old-location: adsi\ads_format_enum.htm
tech.root: adsi
ms.assetid: d0c94f30-6b8c-4c7a-bb74-205b2b658dbb
ms.date: 12/05/2018
ms.keywords: ADS_FORMAT_ENUM, ADS_FORMAT_ENUM enumeration [ADSI], ADS_FORMAT_LEAF, ADS_FORMAT_PROVIDER, ADS_FORMAT_SERVER, ADS_FORMAT_WINDOWS, ADS_FORMAT_WINDOWS_DN, ADS_FORMAT_WINDOWS_NO_SERVER, ADS_FORMAT_WINDOWS_PARENT, ADS_FORMAT_X500, ADS_FORMAT_X500_DN, ADS_FORMAT_X500_NO_SERVER, ADS_FORMAT_X500_PARENT, _ds_ads_format_enum, adsi.ads__format__enum, adsi.ads_format_enum, iads/ADS_FORMAT_ENUM, iads/ADS_FORMAT_LEAF, iads/ADS_FORMAT_PROVIDER, iads/ADS_FORMAT_SERVER, iads/ADS_FORMAT_WINDOWS, iads/ADS_FORMAT_WINDOWS_DN, iads/ADS_FORMAT_WINDOWS_NO_SERVER, iads/ADS_FORMAT_WINDOWS_PARENT, iads/ADS_FORMAT_X500, iads/ADS_FORMAT_X500_DN, iads/ADS_FORMAT_X500_NO_SERVER, iads/ADS_FORMAT_X500_PARENT
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
req.typenames: ADS_FORMAT_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0001_0078_0002
 - iads/__MIDL___MIDL_itf_ads_0001_0078_0002
 - ADS_FORMAT_ENUM
 - iads/ADS_FORMAT_ENUM
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
 - ADS_FORMAT_ENUM
---

# ADS_FORMAT_ENUM enumeration


## -description

The <b>ADS_FORMAT_ENUM</b> enumeration specifies the available path value types used by the  <a href="/windows/desktop/api/iads/nf-iads-iadspathname-retrieve">IADsPathname::Retrieve</a> method.

## -enum-fields

### -field ADS_FORMAT_WINDOWS:1

Returns the full path in Windows format, for example, "LDAP://servername/o=internet/…/cn=bar".

### -field ADS_FORMAT_WINDOWS_NO_SERVER:2

Returns Windows format without server, for example, "LDAP://o=internet/…/cn=bar".

### -field ADS_FORMAT_WINDOWS_DN:3

Returns Windows format of the distinguished name only, for example, "o=internet/…/cn=bar".

### -field ADS_FORMAT_WINDOWS_PARENT:4

Returns Windows format of Parent only, for example, "o=internet/…".

### -field ADS_FORMAT_X500:5

Returns the full path in X.500 format, for example, "LDAP://servername/cn=bar,…,o=internet".

### -field ADS_FORMAT_X500_NO_SERVER:6

Returns the path without server in X.500 format, for example, "LDAP://cn=bar,…,o=internet".

### -field ADS_FORMAT_X500_DN:7

Returns only the distinguished name in X.500 format. For example, "cn=bar,…,o=internet".

### -field ADS_FORMAT_X500_PARENT:8

Returns only the parent in X.500 format, for example, "…,o=internet".

### -field ADS_FORMAT_SERVER:9

Returns the server name, for example, "servername".

### -field ADS_FORMAT_PROVIDER:10

Returns the name of the provider, for example, "LDAP".

### -field ADS_FORMAT_LEAF:11

Returns the name of the leaf, for example, "cn=bar".

## -remarks

The WinNT provider does not support any of the X.500 format specifiers.

Because Visual Basic Scripting Edition  cannot read data from a type library, VBScript applications cannot recognize the symbolic constants as defined above. You should use the numeric constants instead to set the appropriate flags in your VBScript applications. To use the symbolic constants as a good programming practice, write explicit declarations of such constants, as done here.

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI Enumerations</a>



<a href="/windows/desktop/api/iads/nf-iads-iadspathname-retrieve">IADsPathname::Retrieve</a>
