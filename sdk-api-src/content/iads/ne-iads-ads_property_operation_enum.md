---
UID: NE:iads.__MIDL___MIDL_itf_ads_0000_0000_0027
title: ADS_PROPERTY_OPERATION_ENUM (iads.h)
description: Specifies ways to update a named property in the cache.
helpviewer_keywords: ["ADS_PROPERTY_APPEND","ADS_PROPERTY_CLEAR","ADS_PROPERTY_DELETE","ADS_PROPERTY_OPERATION_ENUM","ADS_PROPERTY_OPERATION_ENUM enumeration [ADSI]","ADS_PROPERTY_UPDATE","_ds_ads_property_operation_enum","adsi.ads__property__operation__enum","adsi.ads_property_operation_enum","iads/ADS_PROPERTY_APPEND","iads/ADS_PROPERTY_CLEAR","iads/ADS_PROPERTY_DELETE","iads/ADS_PROPERTY_OPERATION_ENUM","iads/ADS_PROPERTY_UPDATE"]
old-location: adsi\ads_property_operation_enum.htm
tech.root: adsi
ms.assetid: fba20292-870d-4948-abf1-225b1230e938
ms.date: 12/05/2018
ms.keywords: ADS_PROPERTY_APPEND, ADS_PROPERTY_CLEAR, ADS_PROPERTY_DELETE, ADS_PROPERTY_OPERATION_ENUM, ADS_PROPERTY_OPERATION_ENUM enumeration [ADSI], ADS_PROPERTY_UPDATE, _ds_ads_property_operation_enum, adsi.ads__property__operation__enum, adsi.ads_property_operation_enum, iads/ADS_PROPERTY_APPEND, iads/ADS_PROPERTY_CLEAR, iads/ADS_PROPERTY_DELETE, iads/ADS_PROPERTY_OPERATION_ENUM, iads/ADS_PROPERTY_UPDATE
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
req.typenames: ADS_PROPERTY_OPERATION_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0000_0000_0027
 - iads/__MIDL___MIDL_itf_ads_0000_0000_0027
 - ADS_PROPERTY_OPERATION_ENUM
 - iads/ADS_PROPERTY_OPERATION_ENUM
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
 - ADS_PROPERTY_OPERATION_ENUM
---

# ADS_PROPERTY_OPERATION_ENUM enumeration


## -description

The <b>ADS_PROPERTY_OPERATION_ENUM</b> enumeration specifies ways to update a named property in the cache.

## -enum-fields

### -field ADS_PROPERTY_CLEAR:1

Instructs the directory service to remove all the property value(s) from the object.

### -field ADS_PROPERTY_UPDATE:2

Instructs the directory service to replace the current value(s) with the specified value(s).

### -field ADS_PROPERTY_APPEND:3

Instructs the directory service to append the specified value(s) to the existing values(s).

When the <b>ADS_PROPERTY_APPEND</b> operation is specified, the new attribute value(s) are automatically committed to the directory service and removed from the local cache. This forces the local cache to be updated from the directory service the next time the attribute value(s) are retrieved.

### -field ADS_PROPERTY_DELETE:4

Instructs the directory service to delete the specified value(s) from the object.

## -remarks

The elements of this enumeration are used with the  <a href="/windows/desktop/api/iads/nf-iads-iads-putex">IADs.PutEx</a> method, the document of which provides an example of how to use these enumerated constants.

Because Visual Basic Scripting Edition (VBScript) cannot read data from a type library, VBScript applications do not recognize the symbolic constants as defined. Use the numeric constants instead to set the appropriate flags in your VBScript applications. To use the symbolic constants as a good programming practice, write explicit declarations of such constants, as done here.

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI
    Enumerations</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-putex">IADs.PutEx</a>
