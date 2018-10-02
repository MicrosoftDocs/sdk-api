---
UID: NS:ncrypt._NCRYPT_KEY_BLOB_HEADER
title: "_NCRYPT_KEY_BLOB_HEADER"
author: windows-sdk-content
description: Contains a key BLOB.
old-location: security\ncrypt_key_blob_header.htm
tech.root: SecCNG
ms.assetid: 387F05A3-C6E2-48EE-8FD0-C0A45E752300
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PNCRYPT_KEY_BLOB_HEADER, NCRYPT_KEY_BLOB_HEADER, NCRYPT_KEY_BLOB_HEADER structure [Security], PNCRYPT_KEY_BLOB_HEADER, PNCRYPT_KEY_BLOB_HEADER structure pointer [Security], _NCRYPT_KEY_BLOB_HEADER, ncrypt/NCRYPT_KEY_BLOB_HEADER, ncrypt/PNCRYPT_KEY_BLOB_HEADER, security.ncrypt_key_blob_header"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - Ncrypt.h
api_name:
 - NCRYPT_KEY_BLOB_HEADER
product: Windows
targetos: Windows
req.typenames: NCRYPT_KEY_BLOB_HEADER, *PNCRYPT_KEY_BLOB_HEADER
req.redist: 
---

# _NCRYPT_KEY_BLOB_HEADER structure


## -description


The <b>NCRYPT_KEY_BLOB_HEADER</b> structure contains a key <b>BLOB</b>. This structure is used by the <a href="https://msdn.microsoft.com/1588eb29-4026-4d1c-8bee-a035df38444a">NCryptExportKey</a> and <a href="https://msdn.microsoft.com/ede0e7e0-cb2c-44c0-b724-58db3480b781">NCryptImportKey</a> functions.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field dwMagic

Identifies the <b>BLOB</b> type. This can be one of the following values.

<ul>
<li>NCRYPT_CIPHER_KEY_BLOB_MAGIC</li>
<li>NCRYPT_PROTECTED_KEY_BLOB_MAGIC</li>
</ul>

### -field cbAlgName

Size, in bytes, of the null-terminated algorithm name, including the terminating zero.


### -field cbKeyData

Size, in bytes, of the <b>BLOB</b>.


## -see-also




<a href="https://msdn.microsoft.com/1588eb29-4026-4d1c-8bee-a035df38444a">NCryptExportKey</a>



<a href="https://msdn.microsoft.com/ede0e7e0-cb2c-44c0-b724-58db3480b781">NCryptImportKey</a>
 

 

