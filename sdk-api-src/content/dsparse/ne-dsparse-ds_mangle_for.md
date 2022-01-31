---
UID: NE:dsparse._DS_MANGLE_FOR
title: DS_MANGLE_FOR (dsparse.h)
description: The DS_MANGLE_FOR enumeration is used to define whether a relative distinguished name is mangled (encoded) and in what form the mangling occurs.
helpviewer_keywords: ["DS_MANGLE_FOR","DS_MANGLE_FOR enumeration [Active Directory]","DS_MANGLE_OBJECT_RDN_FOR_DELETION","DS_MANGLE_OBJECT_RDN_FOR_NAME_CONFLICT","DS_MANGLE_UNKNOWN","_glines_ds_mangle_for","ad.ds__mangle__for","ad.ds_mangle_for","dsparse/DS_MANGLE_FOR","dsparse/DS_MANGLE_OBJECT_RDN_FOR_DELETION","dsparse/DS_MANGLE_OBJECT_RDN_FOR_NAME_CONFLICT","dsparse/DS_MANGLE_UNKNOWN"]
old-location: ad\ds_mangle_for.htm
tech.root: ad
ms.assetid: 79a66a54-889e-464e-8199-ad911ea84a86
ms.date: 12/05/2018
ms.keywords: DS_MANGLE_FOR, DS_MANGLE_FOR enumeration [Active Directory], DS_MANGLE_OBJECT_RDN_FOR_DELETION, DS_MANGLE_OBJECT_RDN_FOR_NAME_CONFLICT, DS_MANGLE_UNKNOWN, _glines_ds_mangle_for, ad.ds__mangle__for, ad.ds_mangle_for, dsparse/DS_MANGLE_FOR, dsparse/DS_MANGLE_OBJECT_RDN_FOR_DELETION, dsparse/DS_MANGLE_OBJECT_RDN_FOR_NAME_CONFLICT, dsparse/DS_MANGLE_UNKNOWN
req.header: dsparse.h
req.include-header: Ntdsapi.h
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
req.typenames: DS_MANGLE_FOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DS_MANGLE_FOR
 - dsparse/_DS_MANGLE_FOR
 - DS_MANGLE_FOR
 - dsparse/DS_MANGLE_FOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dsparse.h
api_name:
 - DS_MANGLE_FOR
---

# DS_MANGLE_FOR enumeration


## -description

The <b>DS_MANGLE_FOR</b> enumeration is used to define whether a 
   relative distinguished name is mangled (encoded) and in what form the mangling occurs.

## -enum-fields

### -field DS_MANGLE_UNKNOWN:0

Indicates that the relative distinguished name is  not mangled or that the type of mangling is 
      unknown.

### -field DS_MANGLE_OBJECT_RDN_FOR_DELETION

Indicates that the relative distinguished name has been mangled for deletion.

### -field DS_MANGLE_OBJECT_RDN_FOR_NAME_CONFLICT

Indicates that the relative distinguished name has been mangled due to a naming conflict.

## -see-also

<a href="/windows/desktop/api/dsparse/nf-dsparse-dscrackunquotedmangledrdna">DsCrackUnquotedMangledRdn</a>



<a href="/windows/desktop/api/dsparse/nf-dsparse-dsismangleddna">DsIsMangledDn</a>



<a href="/windows/desktop/api/dsparse/nf-dsparse-dsismangledrdnvaluea">DsIsMangledRdnValue</a>



<a href="/windows/desktop/AD/enumerations-in-active-directory-domain-services">Enumerations in Active Directory Domain Services</a>
