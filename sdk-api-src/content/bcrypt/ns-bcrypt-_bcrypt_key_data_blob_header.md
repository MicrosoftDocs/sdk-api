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

# _BCRYPT_KEY_DATA_BLOB_HEADER structure


## -description


The <b>BCRYPT_KEY_DATA_BLOB_HEADER</b> structure is used to contain information about a key data BLOB. The key data BLOB must immediately follow this structure in memory.


## -struct-fields




### -field dwMagic

The magic value for the key.


This member must be the following value.





#### BCRYPT_KEY_DATA_BLOB_MAGIC (0x4d42444b)


### -field dwVersion

Contains the numeric version of the key.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_KEY_DATA_BLOB_VERSION1"></a><a id="bcrypt_key_data_blob_version1"></a><dl>
<dt><b>BCRYPT_KEY_DATA_BLOB_VERSION1</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Version 1.

</td>
</tr>
</table>
 


### -field cbKeyData

The size, in bytes, of the key data.


## -see-also




<a href="https://msdn.microsoft.com/a5d73143-c1d6-43b3-a724-7e27c68a5ade">BCryptExportKey</a>



<a href="https://msdn.microsoft.com/6b9683f4-10f2-40e4-9757-a1f01991bef7">BCryptImportKey</a>
 

 

