---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0050_0001
title: ADS_NAME_TYPE_ENUM (iads.h)
description: Specifies the formats used for representing distinguished names.
helpviewer_keywords: ["ADS_NAME_TYPE_1779","ADS_NAME_TYPE_CANONICAL","ADS_NAME_TYPE_CANONICAL_EX","ADS_NAME_TYPE_DISPLAY","ADS_NAME_TYPE_DOMAIN_SIMPLE","ADS_NAME_TYPE_ENTERPRISE_SIMPLE","ADS_NAME_TYPE_ENUM","ADS_NAME_TYPE_ENUM enumeration [ADSI]","ADS_NAME_TYPE_GUID","ADS_NAME_TYPE_NT4","ADS_NAME_TYPE_SERVICE_PRINCIPAL_NAME","ADS_NAME_TYPE_SID_OR_SID_HISTORY_NAME","ADS_NAME_TYPE_UNKNOWN","ADS_NAME_TYPE_USER_PRINCIPAL_NAME","_ds_ads_name_type_enum","adsi.ads__name__type__enum","adsi.ads_name_type_enum","iads/ADS_NAME_TYPE_1779","iads/ADS_NAME_TYPE_CANONICAL","iads/ADS_NAME_TYPE_CANONICAL_EX","iads/ADS_NAME_TYPE_DISPLAY","iads/ADS_NAME_TYPE_DOMAIN_SIMPLE","iads/ADS_NAME_TYPE_ENTERPRISE_SIMPLE","iads/ADS_NAME_TYPE_ENUM","iads/ADS_NAME_TYPE_GUID","iads/ADS_NAME_TYPE_NT4","iads/ADS_NAME_TYPE_SERVICE_PRINCIPAL_NAME","iads/ADS_NAME_TYPE_SID_OR_SID_HISTORY_NAME","iads/ADS_NAME_TYPE_UNKNOWN","iads/ADS_NAME_TYPE_USER_PRINCIPAL_NAME"]
old-location: adsi\ads_name_type_enum.htm
tech.root: adsi
ms.assetid: 8c5e8f2a-e805-463e-9583-96732d70b209
ms.date: 12/05/2018
ms.keywords: ADS_NAME_TYPE_1779, ADS_NAME_TYPE_CANONICAL, ADS_NAME_TYPE_CANONICAL_EX, ADS_NAME_TYPE_DISPLAY, ADS_NAME_TYPE_DOMAIN_SIMPLE, ADS_NAME_TYPE_ENTERPRISE_SIMPLE, ADS_NAME_TYPE_ENUM, ADS_NAME_TYPE_ENUM enumeration [ADSI], ADS_NAME_TYPE_GUID, ADS_NAME_TYPE_NT4, ADS_NAME_TYPE_SERVICE_PRINCIPAL_NAME, ADS_NAME_TYPE_SID_OR_SID_HISTORY_NAME, ADS_NAME_TYPE_UNKNOWN, ADS_NAME_TYPE_USER_PRINCIPAL_NAME, _ds_ads_name_type_enum, adsi.ads__name__type__enum, adsi.ads_name_type_enum, iads/ADS_NAME_TYPE_1779, iads/ADS_NAME_TYPE_CANONICAL, iads/ADS_NAME_TYPE_CANONICAL_EX, iads/ADS_NAME_TYPE_DISPLAY, iads/ADS_NAME_TYPE_DOMAIN_SIMPLE, iads/ADS_NAME_TYPE_ENTERPRISE_SIMPLE, iads/ADS_NAME_TYPE_ENUM, iads/ADS_NAME_TYPE_GUID, iads/ADS_NAME_TYPE_NT4, iads/ADS_NAME_TYPE_SERVICE_PRINCIPAL_NAME, iads/ADS_NAME_TYPE_SID_OR_SID_HISTORY_NAME, iads/ADS_NAME_TYPE_UNKNOWN, iads/ADS_NAME_TYPE_USER_PRINCIPAL_NAME
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
req.typenames: ADS_NAME_TYPE_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0001_0050_0001
 - iads/__MIDL___MIDL_itf_ads_0001_0050_0001
 - ADS_NAME_TYPE_ENUM
 - iads/ADS_NAME_TYPE_ENUM
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
 - ADS_NAME_TYPE_ENUM
---

# ADS_NAME_TYPE_ENUM enumeration


## -description

The <b>ADS_NAME_TYPE_ENUM</b> enumeration specifies the formats used for representing distinguished names. It is used by the  <a href="/windows/desktop/api/iads/nn-iads-iadsnametranslate">IADsNameTranslate</a> interface to convert the format of a distinguished name.

## -enum-fields

### -field ADS_NAME_TYPE_1779:1

Name format as specified in RFC 1779. For example, "CN=Jeff Smith,CN=users,DC=Fabrikam,DC=com".

### -field ADS_NAME_TYPE_CANONICAL:2

Canonical name format. For example, "Fabrikam.com/Users/Jeff Smith".

### -field ADS_NAME_TYPE_NT4:3

Account name format used in Windows. For example, "Fabrikam\JeffSmith".

### -field ADS_NAME_TYPE_DISPLAY:4

Display name format. For example, "Jeff Smith".

### -field ADS_NAME_TYPE_DOMAIN_SIMPLE:5

Simple domain name format. For example, "JeffSmith@Fabrikam.com".

### -field ADS_NAME_TYPE_ENTERPRISE_SIMPLE:6

Simple enterprise name format. For example, "JeffSmith@Fabrikam.com".

### -field ADS_NAME_TYPE_GUID:7

Global Unique Identifier format. For example, "{95ee9fff-3436-11d1-b2b0-d15ae3ac8436}".

### -field ADS_NAME_TYPE_UNKNOWN:8

Unknown name type. The system will estimate the format. This element is a meaningful option only with the <a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-set">IADsNameTranslate.Set</a> or the <a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-setex">IADsNameTranslate.SetEx</a> method, but not with the <a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-get">IADsNameTranslate.Get</a> or <a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-getex">IADsNameTranslate.GetEx</a> method.

### -field ADS_NAME_TYPE_USER_PRINCIPAL_NAME:9

User principal name format. For example, "JeffSmith@Fabrikam.com".

### -field ADS_NAME_TYPE_CANONICAL_EX:10

Extended canonical name format. For example, "Fabrikam.com/Users Jeff Smith".

### -field ADS_NAME_TYPE_SERVICE_PRINCIPAL_NAME:11

Service principal name format. For example, "www/www.fabrikam.com@fabrikam.com".

### -field ADS_NAME_TYPE_SID_OR_SID_HISTORY_NAME:12

A SID string, as defined in the Security Descriptor Definition Language (SDDL), for either the SID of the current object or one from the object SID history. For example, "O:AOG:DAD:(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-0-0)" For more information, see  <a href="/windows/desktop/SecAuthZ/security-descriptor-string-format">Security Descriptor String Format</a>.

## -remarks

Code examples written in C++, Visual Basic, and VBS/ASP can be found in the discussions of the <a href="/windows/desktop/api/iads/nn-iads-iadsnametranslate">IADsNameTranslate</a> interface.

Because VBScript cannot read data from a type library, an application must use the appropriate numeric constants, instead of the symbolic constants, to set the appropriate flags. To use the symbolic constants as a good programming practice, write explicit declarations of such constants, as done here, in  VBScript applications.

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI
    Enumerations</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsnametranslate">IADsNameTranslate</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-get">IADsNameTranslate.Get</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-getex">IADsNameTranslate.GetEx</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-set">IADsNameTranslate.Set</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-setex">IADsNameTranslate.SetEx</a>



<a href="/windows/desktop/SecAuthZ/security-descriptor-string-format">Security Descriptor String Format</a>
