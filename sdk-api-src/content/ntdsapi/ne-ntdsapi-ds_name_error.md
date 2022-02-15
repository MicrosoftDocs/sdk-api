---
UID: NE:ntdsapi.__unnamed_enum_2
title: DS_NAME_ERROR (ntdsapi.h)
description: The DS_NAME_ERROR enumeration defines the errors returned by the status member of the DS_NAME_RESULT_ITEM structure. These are potential errors that may be encountered while a name is converted by the DsCrackNames function.
helpviewer_keywords: ["DS_NAME_ERROR","DS_NAME_ERROR enumeration [Active Directory]","DS_NAME_ERROR_DOMAIN_ONLY","DS_NAME_ERROR_NOT_FOUND","DS_NAME_ERROR_NOT_UNIQUE","DS_NAME_ERROR_NO_MAPPING","DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING","DS_NAME_ERROR_RESOLVING","DS_NAME_ERROR_TRUST_REFERRAL","DS_NAME_NO_ERROR","_glines_ds_name_error","ad.ds__name__error","ad.ds_name_error","ntdsapi/DS_NAME_ERROR","ntdsapi/DS_NAME_ERROR_DOMAIN_ONLY","ntdsapi/DS_NAME_ERROR_NOT_FOUND","ntdsapi/DS_NAME_ERROR_NOT_UNIQUE","ntdsapi/DS_NAME_ERROR_NO_MAPPING","ntdsapi/DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING","ntdsapi/DS_NAME_ERROR_RESOLVING","ntdsapi/DS_NAME_ERROR_TRUST_REFERRAL","ntdsapi/DS_NAME_NO_ERROR"]
old-location: ad\ds_name_error.htm
tech.root: ad
ms.assetid: 8475133c-4bc8-4545-bd54-15d4e7b07869
ms.date: 12/05/2018
ms.keywords: DS_NAME_ERROR, DS_NAME_ERROR enumeration [Active Directory], DS_NAME_ERROR_DOMAIN_ONLY, DS_NAME_ERROR_NOT_FOUND, DS_NAME_ERROR_NOT_UNIQUE, DS_NAME_ERROR_NO_MAPPING, DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING, DS_NAME_ERROR_RESOLVING, DS_NAME_ERROR_TRUST_REFERRAL, DS_NAME_NO_ERROR, _glines_ds_name_error, ad.ds__name__error, ad.ds_name_error, ntdsapi/DS_NAME_ERROR, ntdsapi/DS_NAME_ERROR_DOMAIN_ONLY, ntdsapi/DS_NAME_ERROR_NOT_FOUND, ntdsapi/DS_NAME_ERROR_NOT_UNIQUE, ntdsapi/DS_NAME_ERROR_NO_MAPPING, ntdsapi/DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING, ntdsapi/DS_NAME_ERROR_RESOLVING, ntdsapi/DS_NAME_ERROR_TRUST_REFERRAL, ntdsapi/DS_NAME_NO_ERROR
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
req.typenames: DS_NAME_ERROR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DS_NAME_ERROR
 - ntdsapi/DS_NAME_ERROR
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
 - DS_NAME_ERROR
---

# DS_NAME_ERROR enumeration


## -description

The <b>DS_NAME_ERROR</b> enumeration defines the errors returned by the <b>status</b> member of the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_result_itema">DS_NAME_RESULT_ITEM</a> structure. These are potential errors that may be encountered while a name is converted by the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackNames</a> function.

## -enum-fields

### -field DS_NAME_NO_ERROR:0

The conversion was successful.

### -field DS_NAME_ERROR_RESOLVING:1

A generic processing error occurred.

### -field DS_NAME_ERROR_NOT_FOUND:2

The name cannot be found or the caller does not have permission to access the name.

### -field DS_NAME_ERROR_NOT_UNIQUE:3

The input name is mapped to more than one output name or the desired format did not have a single, unique value for the object found.

### -field DS_NAME_ERROR_NO_MAPPING:4

The input name was found, but the associated output format cannot be found. This can occur if the object does not have all the required attributes.

### -field DS_NAME_ERROR_DOMAIN_ONLY:5

Unable to resolve entire name, but was able to determine in which domain object resides. The caller is expected to retry the call at a domain controller for the specified domain. The entire name cannot be resolved, but the domain that the object resides in could be determined. The <b>pDomain</b> member of the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_result_itema">DS_NAME_RESULT_ITEM</a> contains valid data when this error is specified.

### -field DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING:6

A syntactical mapping cannot be performed on the client without transmitting over the network.

### -field DS_NAME_ERROR_TRUST_REFERRAL:7

The name is from an external trusted forest.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_result_itema">DS_NAME_RESULT_ITEM</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackNames</a>



<a href="/windows/desktop/AD/enumerations-in-active-directory-domain-services">Enumerations in Active Directory Domain Services</a>
