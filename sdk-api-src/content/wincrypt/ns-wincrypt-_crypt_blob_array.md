---
UID: NS:wincrypt._CRYPT_BLOB_ARRAY
title: "_CRYPT_BLOB_ARRAY"
author: windows-driver-content
description: Contains an array of CRYPT_DATA_BLOB structures.
old-location: security\crypt_blob_array.htm
old-project: SecCrypto
ms.assetid: c4429a0c-6e79-4f02-acac-42b5280aa3b1
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: "*PCRYPT_BLOB_ARRAY, CRYPT_BLOB_ARRAY, CRYPT_BLOB_ARRAY structure [Security], PCRYPT_BLOB_ARRAY, PCRYPT_BLOB_ARRAY structure pointer [Security], _CRYPT_BLOB_ARRAY, security.crypt_blob_array, wincrypt/CRYPT_BLOB_ARRAY, wincrypt/PCRYPT_BLOB_ARRAY"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: CRYPT_BLOB_ARRAY, *PCRYPT_BLOB_ARRAY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CRYPT_BLOB_ARRAY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CRYPT_BLOB_ARRAY structure


## -description


The <b>CRYPT_BLOB_ARRAY</b> structure contains an array of <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structures.


## -struct-fields




### -field cBlob

The number of elements in the <b>rgBlob</b> array.


### -field rgBlob

An array of <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structures that contains the data blobs.

