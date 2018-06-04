---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

