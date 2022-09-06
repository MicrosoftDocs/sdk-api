---
UID: NE:ntdsapi.__unnamed_enum_1
title: DS_NAME_FLAGS (ntdsapi.h)
description: The DS_NAME_FLAGS enumeration is used to define how the name syntax will be cracked. These flags are used by the DsCrackNames function.
helpviewer_keywords: ["DS_NAME_FLAGS","DS_NAME_FLAGS enumeration [Active Directory]","DS_NAME_FLAG_EVAL_AT_DC","DS_NAME_FLAG_GCVERIFY","DS_NAME_FLAG_SYNTACTICAL_ONLY","DS_NAME_FLAG_TRUST_REFERRAL","DS_NAME_NO_FLAGS","_glines_ds_name_flags","ad.ds__name__flags","ad.ds_name_flags","ntdsapi/DS_NAME_FLAGS","ntdsapi/DS_NAME_FLAG_EVAL_AT_DC","ntdsapi/DS_NAME_FLAG_GCVERIFY","ntdsapi/DS_NAME_FLAG_SYNTACTICAL_ONLY","ntdsapi/DS_NAME_FLAG_TRUST_REFERRAL","ntdsapi/DS_NAME_NO_FLAGS"]
old-location: ad\ds_name_flags.htm
tech.root: ad
ms.assetid: f0108568-4a6a-4159-b55f-2c651c588b73
ms.date: 12/05/2018
ms.keywords: DS_NAME_FLAGS, DS_NAME_FLAGS enumeration [Active Directory], DS_NAME_FLAG_EVAL_AT_DC, DS_NAME_FLAG_GCVERIFY, DS_NAME_FLAG_SYNTACTICAL_ONLY, DS_NAME_FLAG_TRUST_REFERRAL, DS_NAME_NO_FLAGS, _glines_ds_name_flags, ad.ds__name__flags, ad.ds_name_flags, ntdsapi/DS_NAME_FLAGS, ntdsapi/DS_NAME_FLAG_EVAL_AT_DC, ntdsapi/DS_NAME_FLAG_GCVERIFY, ntdsapi/DS_NAME_FLAG_SYNTACTICAL_ONLY, ntdsapi/DS_NAME_FLAG_TRUST_REFERRAL, ntdsapi/DS_NAME_NO_FLAGS
req.header: ntdsapi.h
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
req.typenames: DS_NAME_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DS_NAME_FLAGS
 - ntdsapi/DS_NAME_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_NAME_FLAGS
---

# DS_NAME_FLAGS enumeration


## -description

The <b>DS_NAME_FLAGS</b> enumeration is used to define how the name syntax will be cracked. These flags are used by the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackNames</a> function.

## -enum-fields

### -field DS_NAME_NO_FLAGS:0x0

Indicates that there are no associated flags.

### -field DS_NAME_FLAG_SYNTACTICAL_ONLY:0x1

Performs a syntactical mapping at the client without transferring over the network. The only syntactic mapping supported is from <a href="/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_name_format">DS_FQDN_1779_NAME</a> to <b>DS_CANONICAL_NAME</b> or <b>DS_CANONICAL_NAME_EX</b>. <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackNames</a> returns the <b>DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING</b> flag if a  syntactical mapping is not possible.

### -field DS_NAME_FLAG_EVAL_AT_DC:0x2

Forces a trip to the domain controller for evaluation, even if the syntax could be cracked locally.

### -field DS_NAME_FLAG_GCVERIFY:0x4

The call fails if the domain controller is not a global catalog server.

### -field DS_NAME_FLAG_TRUST_REFERRAL:0x8

Enables cross forest trust referral.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_name_format">DS_NAME_FORMAT</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackNames</a>



<a href="/windows/desktop/AD/enumerations-in-active-directory-domain-services">Enumerations in Active Directory Domain Services</a>
