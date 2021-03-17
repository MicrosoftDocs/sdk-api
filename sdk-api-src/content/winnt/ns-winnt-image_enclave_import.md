---
UID: NS:winnt._IMAGE_ENCLAVE_IMPORT
title: IMAGE_ENCLAVE_IMPORT (winnt.h)
description: Defines a entry in the array of images that an enclave can import.
helpviewer_keywords: ["*PIMAGE_ENCLAVE_IMPORT","IMAGE_ENCLAVE_IMPORT","IMAGE_ENCLAVE_IMPORT structure","IMAGE_ENCLAVE_IMPORT_MATCH_AUTHOR_ID","IMAGE_ENCLAVE_IMPORT_MATCH_FAMILY_ID","IMAGE_ENCLAVE_IMPORT_MATCH_IMAGE_ID","IMAGE_ENCLAVE_IMPORT_MATCH_NONE","IMAGE_ENCLAVE_IMPORT_MATCH_UNIQUE_ID","PIMAGE_ENCLAVE_IMPORT","PIMAGE_ENCLAVE_IMPORT structure pointer","base.image_enclave_import","winnt/IMAGE_ENCLAVE_IMPORT","winnt/PIMAGE_ENCLAVE_IMPORT"]
old-location: base\image_enclave_import.htm
tech.root: base
ms.assetid: 32E75114-61B2-4051-99EC-873DD75A368A
ms.date: 12/05/2018
ms.keywords: '*PIMAGE_ENCLAVE_IMPORT, IMAGE_ENCLAVE_IMPORT, IMAGE_ENCLAVE_IMPORT structure, IMAGE_ENCLAVE_IMPORT_MATCH_AUTHOR_ID, IMAGE_ENCLAVE_IMPORT_MATCH_FAMILY_ID, IMAGE_ENCLAVE_IMPORT_MATCH_IMAGE_ID, IMAGE_ENCLAVE_IMPORT_MATCH_NONE, IMAGE_ENCLAVE_IMPORT_MATCH_UNIQUE_ID, PIMAGE_ENCLAVE_IMPORT, PIMAGE_ENCLAVE_IMPORT structure pointer, base.image_enclave_import, winnt/IMAGE_ENCLAVE_IMPORT, winnt/PIMAGE_ENCLAVE_IMPORT'
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: IMAGE_ENCLAVE_IMPORT, *PIMAGE_ENCLAVE_IMPORT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IMAGE_ENCLAVE_IMPORT
 - winnt/_IMAGE_ENCLAVE_IMPORT
 - PIMAGE_ENCLAVE_IMPORT
 - winnt/PIMAGE_ENCLAVE_IMPORT
 - IMAGE_ENCLAVE_IMPORT
 - winnt/IMAGE_ENCLAVE_IMPORT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winnt.h
api_name:
 - IMAGE_ENCLAVE_IMPORT
---

# IMAGE_ENCLAVE_IMPORT structure


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

