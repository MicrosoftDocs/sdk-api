---
UID: NS:bcrypt._BCRYPT_OID
title: BCRYPT_OID (bcrypt.h)

description: Contains information about a DER-encoded object identifier (OID).
old-location: security\bcrypt_oid.htm
tech.root: SecCNG
ms.assetid: 00143883-88f7-4b15-bdba-128ee255abf6

ms.date: 12/05/2018
ms.keywords: BCRYPT_OID, BCRYPT_OID structure [Security], bcrypt/BCRYPT_OID, security.bcrypt_oid
ms.topic: struct
f1_keywords:
- bcrypt/BCRYPT_OID
dev_langs:
 - c++
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- Bcrypt.h
api_name:
- BCRYPT_OID
targetos: Windows
req.typenames: BCRYPT_OID
req.redist: 
ms.custom: 19H1
---

# BCRYPT_OID structure


## -description


The <b>BCRYPT_OID</b> structure contains information about a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">DER</a>-encoded <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID). CNG uses  hash OIDs in functions that sign or verify data in <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">PKCS #1</a> format.


## -struct-fields




### -field cbOID

The size, in bytes, of the <b>pbOID</b> buffer.


### -field pbOID

The address of a buffer that contains the OID.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCNG/cng-property-identifiers">BCRYPT_HASH_OID_LIST</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_oid_list">BCRYPT_OID_LIST</a>
 

 

