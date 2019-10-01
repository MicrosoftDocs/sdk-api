---
UID: NS:wincrypt._CRYPT_BLOB_ARRAY
title: CRYPT_BLOB_ARRAY (wincrypt.h)
author: windows-sdk-content
description: Contains an array of CRYPT_DATA_BLOB structures.
old-location: security\crypt_blob_array.htm
tech.root: SecCrypto
ms.assetid: c4429a0c-6e79-4f02-acac-42b5280aa3b1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCRYPT_BLOB_ARRAY, CRYPT_BLOB_ARRAY, CRYPT_BLOB_ARRAY structure [Security], PCRYPT_BLOB_ARRAY, PCRYPT_BLOB_ARRAY structure pointer [Security], security.crypt_blob_array, wincrypt/CRYPT_BLOB_ARRAY, wincrypt/PCRYPT_BLOB_ARRAY"
ms.topic: struct
f1_keywords: 
 - "wincrypt/CRYPT_BLOB_ARRAY"
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Wincrypt.h
api_name:
 - CRYPT_BLOB_ARRAY
targetos: Windows
req.typenames: CRYPT_BLOB_ARRAY, *PCRYPT_BLOB_ARRAY
req.redist: 
ms.custom: 19H1
---

# CRYPT_BLOB_ARRAY structure


## -description


The <b>CRYPT_BLOB_ARRAY</b> structure contains an array of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structures.


## -struct-fields




### -field cBlob

The number of elements in the <b>rgBlob</b> array.


### -field rgBlob

An array of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structures that contains the data blobs.

