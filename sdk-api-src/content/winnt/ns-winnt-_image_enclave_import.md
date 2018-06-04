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

# _IMAGE_ENCLAVE_IMPORT structure


## -description


Defines a entry in the array of images that an enclave can import.


## -struct-fields




### -field MatchType

The type of identifier of the image that must match the value in the import record.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IMAGE_ENCLAVE_IMPORT_MATCH_NONE"></a><a id="image_enclave_import_match_none"></a><dl>
<dt><b>IMAGE_ENCLAVE_IMPORT_MATCH_NONE</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
None of the identifiers of the image need to match the value in the import record.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_ENCLAVE_IMPORT_MATCH_UNIQUE_ID"></a><a id="image_enclave_import_match_unique_id"></a><dl>
<dt><b>IMAGE_ENCLAVE_IMPORT_MATCH_UNIQUE_ID</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The value of the enclave unique identifier of the image must match the value in the import record. Otherwise, loading of the image fails.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_ENCLAVE_IMPORT_MATCH_AUTHOR_ID"></a><a id="image_enclave_import_match_author_id"></a><dl>
<dt><b>IMAGE_ENCLAVE_IMPORT_MATCH_AUTHOR_ID</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The value of the enclave author identifier of the image must match the value in the import record. Otherwise, loading of the image fails. If this flag is set and the import record indicates an author identifier of all zeros, the imported image must be part of the Windows installation.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_ENCLAVE_IMPORT_MATCH_FAMILY_ID"></a><a id="image_enclave_import_match_family_id"></a><dl>
<dt><b>IMAGE_ENCLAVE_IMPORT_MATCH_FAMILY_ID</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
The value of the enclave family identifier of the image must match the value in the import record. Otherwise, loading of the image fails.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_ENCLAVE_IMPORT_MATCH_IMAGE_ID"></a><a id="image_enclave_import_match_image_id"></a><dl>
<dt><b>IMAGE_ENCLAVE_IMPORT_MATCH_IMAGE_ID</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The value of the enclave image identifier must match the value in the import record. Otherwise, loading of the image fails.

</td>
</tr>
</table>
 


### -field MinimumSecurityVersion

The minimum enclave security version that each image must have for the image to be imported successfully. The image is rejected unless its enclave security version is equal to or greater than the minimum value in the import record.  Set the value in the import record to zero to turn off the security version check. 


### -field UniqueOrAuthorID

The unique identifier of the primary module for the enclave, if the <b>MatchType</b> member is <b>IMAGE_ENCLAVE_IMPORT_MATCH_UNIQUE_ID</b>. Otherwise, the author identifier of the primary module for the enclave..


### -field FamilyID

The family identifier of the primary module for the enclave.


### -field ImageID

The image identifier of the primary module for the enclave.


### -field ImportName

The relative virtual address of a NULL-terminated string that contains the same value found in the import directory for the image.


### -field Reserved

Reserved.

