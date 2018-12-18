---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0050_0001
title: ADS_NAME_TYPE_ENUM
author: windows-sdk-content
description: Specifies the formats used for representing distinguished names.
old-location: adsi\ads_name_type_enum.htm
tech.root: adsi
ms.assetid: 8c5e8f2a-e805-463e-9583-96732d70b209
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ADS_NAME_TYPE_1779, ADS_NAME_TYPE_CANONICAL, ADS_NAME_TYPE_CANONICAL_EX, ADS_NAME_TYPE_DISPLAY, ADS_NAME_TYPE_DOMAIN_SIMPLE, ADS_NAME_TYPE_ENTERPRISE_SIMPLE, ADS_NAME_TYPE_ENUM, ADS_NAME_TYPE_ENUM enumeration [ADSI], ADS_NAME_TYPE_GUID, ADS_NAME_TYPE_NT4, ADS_NAME_TYPE_SERVICE_PRINCIPAL_NAME, ADS_NAME_TYPE_SID_OR_SID_HISTORY_NAME, ADS_NAME_TYPE_UNKNOWN, ADS_NAME_TYPE_USER_PRINCIPAL_NAME, _ds_ads_name_type_enum, adsi.ads__name__type__enum, adsi.ads_name_type_enum, iads/ADS_NAME_TYPE_1779, iads/ADS_NAME_TYPE_CANONICAL, iads/ADS_NAME_TYPE_CANONICAL_EX, iads/ADS_NAME_TYPE_DISPLAY, iads/ADS_NAME_TYPE_DOMAIN_SIMPLE, iads/ADS_NAME_TYPE_ENTERPRISE_SIMPLE, iads/ADS_NAME_TYPE_ENUM, iads/ADS_NAME_TYPE_GUID, iads/ADS_NAME_TYPE_NT4, iads/ADS_NAME_TYPE_SERVICE_PRINCIPAL_NAME, iads/ADS_NAME_TYPE_SID_OR_SID_HISTORY_NAME, iads/ADS_NAME_TYPE_UNKNOWN, iads/ADS_NAME_TYPE_USER_PRINCIPAL_NAME
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_NAME_TYPE_ENUM
product: Windows
targetos: Windows
req.typenames: ADS_NAME_TYPE_ENUM
req.redist: 
---

# ADS_NAME_TYPE_ENUM enumeration


## -description


The <b>ADS_NAME_TYPE_ENUM</b> enumeration specifies the formats used for representing distinguished names. It is used by the  <a href="https://msdn.microsoft.com/3d8baeb1-0edc-4648-8691-6ea4dcfd8f62">IADsNameTranslate</a> interface to convert the format of a distinguished name.


## -enum-fields




### -field ADS_NAME_TYPE_1779

Name format as specified in RFC 1779. For example, "CN=Jeff Smith,CN=users,DC=Fabrikam,DC=com".


### -field ADS_NAME_TYPE_CANONICAL

Canonical name format. For example, "Fabrikam.com/Users/Jeff Smith".


### -field ADS_NAME_TYPE_NT4

Account name format used in Windows. For example, "Fabrikam\JeffSmith".


### -field ADS_NAME_TYPE_DISPLAY

Display name format. For example, "Jeff Smith".


### -field ADS_NAME_TYPE_DOMAIN_SIMPLE

Simple domain name format. For example, "JeffSmith@Fabrikam.com".


### -field ADS_NAME_TYPE_ENTERPRISE_SIMPLE

Simple enterprise name format. For example, "JeffSmith@Fabrikam.com".


### -field ADS_NAME_TYPE_GUID

Global Unique Identifier format. For example, "{95ee9fff-3436-11d1-b2b0-d15ae3ac8436}".


### -field ADS_NAME_TYPE_UNKNOWN

Unknown name type. The system will estimate the format. This element is a meaningful option only with the <a href="https://msdn.microsoft.com/1c126333-3d5c-4ba3-8c66-de778e26488f">IADsNameTranslate.Set</a> or the <a href="https://msdn.microsoft.com/e8a5014e-d848-46b7-a336-7801ff1f6b08">IADsNameTranslate.SetEx</a> method, but not with the <a href="https://msdn.microsoft.com/6c8246a9-657e-4db1-ae8f-d9c0a2d41397">IADsNameTranslate.Get</a> or <a href="https://msdn.microsoft.com/01c4fc79-ed5b-4a24-9b97-25b4095a9c8f">IADsNameTranslate.GetEx</a> method.


### -field ADS_NAME_TYPE_USER_PRINCIPAL_NAME

User principal name format. For example, "JeffSmith@Fabrikam.com".


### -field ADS_NAME_TYPE_CANONICAL_EX

Extended canonical name format. For example, "Fabrikam.com/Users Jeff Smith".


### -field ADS_NAME_TYPE_SERVICE_PRINCIPAL_NAME

Service principal name format. For example, "www/www.fabrikam.com@fabrikam.com".


### -field ADS_NAME_TYPE_SID_OR_SID_HISTORY_NAME

A SID string, as defined in the Security Descriptor Definition Language (SDDL), for either the SID of the current object or one from the object SID history. For example, "O:AOG:DAD:(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-0-0)" For more information, see  <a href="https://msdn.microsoft.com/0a226629-084c-40c5-bdd4-ad7355c807cf">Security Descriptor String Format</a>.


## -remarks



Code examples written in C++, Visual Basic, and VBS/ASP can be found in the discussions of the <a href="https://msdn.microsoft.com/3d8baeb1-0edc-4648-8691-6ea4dcfd8f62">IADsNameTranslate</a> interface.

Because VBScript cannot read data from a type library, an application must use the appropriate numeric constants, instead of the symbolic constants, to set the appropriate flags. To use the symbolic constants as a good programming practice, write explicit declarations of such constants, as done here, in  VBScript applications.




## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI
    Enumerations</a>



<a href="https://msdn.microsoft.com/3d8baeb1-0edc-4648-8691-6ea4dcfd8f62">IADsNameTranslate</a>



<a href="https://msdn.microsoft.com/6c8246a9-657e-4db1-ae8f-d9c0a2d41397">IADsNameTranslate.Get</a>



<a href="https://msdn.microsoft.com/01c4fc79-ed5b-4a24-9b97-25b4095a9c8f">IADsNameTranslate.GetEx</a>



<a href="https://msdn.microsoft.com/1c126333-3d5c-4ba3-8c66-de778e26488f">IADsNameTranslate.Set</a>



<a href="https://msdn.microsoft.com/e8a5014e-d848-46b7-a336-7801ff1f6b08">IADsNameTranslate.SetEx</a>



<a href="https://msdn.microsoft.com/0a226629-084c-40c5-bdd4-ad7355c807cf">Security Descriptor String Format</a>
 

 

