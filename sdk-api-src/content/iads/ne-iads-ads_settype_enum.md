---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0078_0001
title: ADS_SETTYPE_ENUM (iads.h)
description: The ADS_SETTYPE_ENUM enumeration specifies the available pathname format used by the IADsPathname::Set method.
helpviewer_keywords: ["ADS_SETTYPE_DN","ADS_SETTYPE_ENUM","ADS_SETTYPE_ENUM enumeration [ADSI]","ADS_SETTYPE_FULL","ADS_SETTYPE_PROVIDER","ADS_SETTYPE_SERVER","_ds_ads_settype_enum","adsi.ads__settype__enum","adsi.ads_settype_enum","iads/ADS_SETTYPE_DN","iads/ADS_SETTYPE_ENUM","iads/ADS_SETTYPE_FULL","iads/ADS_SETTYPE_PROVIDER","iads/ADS_SETTYPE_SERVER"]
old-location: adsi\ads_settype_enum.htm
tech.root: adsi
ms.assetid: fbf7de54-3ea7-4d66-ad56-21cae1e28c07
ms.date: 12/05/2018
ms.keywords: ADS_SETTYPE_DN, ADS_SETTYPE_ENUM, ADS_SETTYPE_ENUM enumeration [ADSI], ADS_SETTYPE_FULL, ADS_SETTYPE_PROVIDER, ADS_SETTYPE_SERVER, _ds_ads_settype_enum, adsi.ads__settype__enum, adsi.ads_settype_enum, iads/ADS_SETTYPE_DN, iads/ADS_SETTYPE_ENUM, iads/ADS_SETTYPE_FULL, iads/ADS_SETTYPE_PROVIDER, iads/ADS_SETTYPE_SERVER
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
req.typenames: ADS_SETTYPE_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0001_0078_0001
 - iads/__MIDL___MIDL_itf_ads_0001_0078_0001
 - ADS_SETTYPE_ENUM
 - iads/ADS_SETTYPE_ENUM
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
 - ADS_SETTYPE_ENUM
---

# ADS_SETTYPE_ENUM enumeration


## -description

The <b>ADS_SETTYPE_ENUM</b> enumeration specifies the available pathname format used by the  <a href="/windows/desktop/api/iads/nf-iads-iadspathname-set">IADsPathname::Set</a> method.

## -enum-fields

### -field ADS_SETTYPE_FULL:1

Sets the full path, for example, "LDAP://servername/o=internet/…/cn=bar".

### -field ADS_SETTYPE_PROVIDER:2

Updates the provider only, for example, "LDAP".

### -field ADS_SETTYPE_SERVER:3

Updates the server name only, for example, "servername".

### -field ADS_SETTYPE_DN:4

Updates the distinguished name only, for example, "o=internet/…/cn=bar".

## -remarks

Since VBScript cannot read information from a type library, VBScript applications do not understand the symbolic constants as defined above. You should use the numerical constants instead to set the appropriate flags in your VBScript applications. If you want to use the symbolic constants as a good programming practice, you should make explicit declarations of such constants, as done here, in your VBScript applications.

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI Enumerations</a>



<a href="/windows/desktop/api/iads/nf-iads-iadspathname-set">IADsPathname::Set</a>
