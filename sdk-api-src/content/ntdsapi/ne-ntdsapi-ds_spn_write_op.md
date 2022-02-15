---
UID: NE:ntdsapi.__unnamed_enum_4
title: DS_SPN_WRITE_OP (ntdsapi.h)
description: The DS_SPN_WRITE_OP enumeration identifies the type of write operation that should be performed by the DsWriteAccountSpn function.
helpviewer_keywords: ["DS_SPN_ADD_SPN_OP","DS_SPN_DELETE_SPN_OP","DS_SPN_REPLACE_SPN_OP","DS_SPN_WRITE_OP","DS_SPN_WRITE_OP enumeration [Active Directory]","_glines_ds_spn_write_op","ad.ds__spn__write__op","ad.ds_spn_write_op","ntdsapi/DS_SPN_ADD_SPN_OP","ntdsapi/DS_SPN_DELETE_SPN_OP","ntdsapi/DS_SPN_REPLACE_SPN_OP","ntdsapi/DS_SPN_WRITE_OP"]
old-location: ad\ds_spn_write_op.htm
tech.root: ad
ms.assetid: 8367bdaf-3d8d-46b3-9d03-b9753e8e5a1a
ms.date: 12/05/2018
ms.keywords: DS_SPN_ADD_SPN_OP, DS_SPN_DELETE_SPN_OP, DS_SPN_REPLACE_SPN_OP, DS_SPN_WRITE_OP, DS_SPN_WRITE_OP enumeration [Active Directory], _glines_ds_spn_write_op, ad.ds__spn__write__op, ad.ds_spn_write_op, ntdsapi/DS_SPN_ADD_SPN_OP, ntdsapi/DS_SPN_DELETE_SPN_OP, ntdsapi/DS_SPN_REPLACE_SPN_OP, ntdsapi/DS_SPN_WRITE_OP
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
req.typenames: DS_SPN_WRITE_OP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DS_SPN_WRITE_OP
 - ntdsapi/DS_SPN_WRITE_OP
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
 - DS_SPN_WRITE_OP
---

# DS_SPN_WRITE_OP enumeration


## -description

The <b>DS_SPN_WRITE_OP</b> enumeration identifies the type of write operation that should be performed by the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dswriteaccountspna">DsWriteAccountSpn</a> function.

## -enum-fields

### -field DS_SPN_ADD_SPN_OP:0

Adds the specified service principal names (SPNs) to the object identified by the <i>pszAccount</i> parameter in <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dswriteaccountspna">DsWriteAccountSpn</a>.

### -field DS_SPN_REPLACE_SPN_OP:1

Removes all SPNs currently registered on the account identified by the <i>pszAccount</i> parameter in <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dswriteaccountspna">DsWriteAccountSpn</a> and replaces them with the SPNs specified  by the <i>rpszSpn</i> parameter in <b>DsWriteAccountSpn</b>.

### -field DS_SPN_DELETE_SPN_OP:2        

Deletes the specified SPNs from the object identified by the <i>pszAccount</i> parameter in <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dswriteaccountspna">DsWriteAccountSpn</a>.

## -see-also

<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dswriteaccountspna">DsWriteAccountSpn</a>



<a href="/windows/desktop/AD/enumerations-in-active-directory-domain-services">Enumerations in Active Directory Domain Services</a>
