---
UID: NS:bcrypt._BCRYPT_OID
title: BCRYPT_OID (bcrypt.h)
author: windows-sdk-content
description: Contains information about a DER-encoded object identifier (OID).
old-location: security\bcrypt_oid.htm
tech.root: SecCNG
ms.assetid: 00143883-88f7-4b15-bdba-128ee255abf6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BCRYPT_OID, BCRYPT_OID structure [Security], bcrypt/BCRYPT_OID, security.bcrypt_oid
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: BCRYPT_OID
req.redist: 
---

# BCRYPT_OID structure


## -description


The <b>BCRYPT_OID</b> structure contains information about a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">DER</a>-encoded <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID). CNG uses  hash OIDs in functions that sign or verify data in <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">PKCS #1</a> format.


## -struct-fields




### -field cbOID

The size, in bytes, of the <b>pbOID</b> buffer.


### -field pbOID

The address of a buffer that contains the OID.


## -see-also




<a href="https://msdn.microsoft.com/ebcc8202-94b4-47ad-9918-e5bc843a258f">BCRYPT_HASH_OID_LIST</a>



<a href="https://msdn.microsoft.com/5e07d4a9-88eb-4644-a9be-e39c52b97ea7">BCRYPT_OID_LIST</a>
 

 

