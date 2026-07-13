---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0048_0004
title: ADS_FLAGTYPE_ENUM (iads.h)
description: The ADS_FLAGTYPE_ENUM enumeration specifies values that can be used to indicate the presence of the ObjectType or InheritedObjectType fields in the access-control entry (ACE).
helpviewer_keywords: ["ADS_FLAGTYPE_ENUM","ADS_FLAGTYPE_ENUM enumeration [ADSI]","ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT","ADS_FLAG_OBJECT_TYPE_PRESENT","_ds_ads_flagtype_enum","adsi.ads__flagtype__enum","adsi.ads_flagtype_enum","iads/ADS_FLAGTYPE_ENUM","iads/ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT","iads/ADS_FLAG_OBJECT_TYPE_PRESENT"]
old-location: adsi\ads_flagtype_enum.htm
tech.root: adsi
ms.assetid: 6c3354d8-8df7-476d-af21-63725e5ed778
ms.date: 12/05/2018
ms.keywords: ADS_FLAGTYPE_ENUM, ADS_FLAGTYPE_ENUM enumeration [ADSI], ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT, ADS_FLAG_OBJECT_TYPE_PRESENT, _ds_ads_flagtype_enum, adsi.ads__flagtype__enum, adsi.ads_flagtype_enum, iads/ADS_FLAGTYPE_ENUM, iads/ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT, iads/ADS_FLAG_OBJECT_TYPE_PRESENT
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
req.typenames: ADS_FLAGTYPE_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0001_0048_0004
 - iads/__MIDL___MIDL_itf_ads_0001_0048_0004
 - ADS_FLAGTYPE_ENUM
 - iads/ADS_FLAGTYPE_ENUM
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
 - ADS_FLAGTYPE_ENUM
---

# ADS_FLAGTYPE_ENUM enumeration


## -description

The <b>ADS_FLAGTYPE_ENUM</b> enumeration specifies values that can be used to indicate the presence of the <b>ObjectType</b> or <b>InheritedObjectType</b> fields in the access-control entry (ACE).

## -enum-fields

### -field ADS_FLAG_OBJECT_TYPE_PRESENT:0x1

The <b>ObjectType</b> field is present in the ACE.

### -field ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT:0x2

The <b>InheritedObjectType</b> field is present in the ACE.

## -remarks

<b>ObjectType</b> indicates what object type, property set, or property an ACE refers to. It takes a GUID as its value. The GUID referenced by <b>ObjectType</b> is not physically present in the ACE unless ADS_FLAGS_OBJECT_TYPE_PRESENT is set.

<b>InheritedObjectType</b> specifies the GUID of an object that will inherit the ACE. The GUID is not physically present in the ACE unless the ADS_FLAG_INHERITED_OBJECT_TYPE_PRESENT bit is set.

<div class="alert"><b>Note</b>  Because VBScript cannot read information from a type library, VBScript applications do not understand the symbolic constants as defined above. You should use the numerical constants instead to set the appropriate flags in your VBScript applications. If you want to use the symbolic constants as a good programming practice, you should make explicit declarations of such constants, as done here, in your VBScript applications.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI Enumerations</a>
