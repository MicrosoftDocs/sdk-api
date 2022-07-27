---
UID: NS:winnt._IMAGE_ENCLAVE_CONFIG64
title: IMAGE_ENCLAVE_CONFIG64 (winnt.h)
description: Defines the format of the enclave configuration for systems running 32-bit Windows. (64 bit)
helpviewer_keywords: ["*PIMAGE_ENCLAVE_CONFIG64","IMAGE_ENCLAVE_CONFIG","IMAGE_ENCLAVE_CONFIG32","IMAGE_ENCLAVE_CONFIG32 structure","IMAGE_ENCLAVE_CONFIG64","IMAGE_ENCLAVE_FLAG_PRIMARY_IMAGE","IMAGE_ENCLAVE_POLICY_DEBUGGABLE","PIMAGE_ENCLAVE_CONFIG32","PIMAGE_ENCLAVE_CONFIG32 structure pointer","_IMAGE_ENCLAVE_CONFIG32","base.image_enclave_config","base.image_enclave_config32","winnt/IMAGE_ENCLAVE_CONFIG32","winnt/PIMAGE_ENCLAVE_CONFIG32"]
old-location: base\image_enclave_config32.htm
tech.root: base
ms.assetid: 6006F018-4F3F-4595-8ED2-89D2CC7F782D
ms.date: 12/05/2018
ms.keywords: '*PIMAGE_ENCLAVE_CONFIG64, IMAGE_ENCLAVE_CONFIG, IMAGE_ENCLAVE_CONFIG32, IMAGE_ENCLAVE_CONFIG32 structure, IMAGE_ENCLAVE_CONFIG64, IMAGE_ENCLAVE_FLAG_PRIMARY_IMAGE, IMAGE_ENCLAVE_POLICY_DEBUGGABLE, PIMAGE_ENCLAVE_CONFIG32, PIMAGE_ENCLAVE_CONFIG32 structure pointer, _IMAGE_ENCLAVE_CONFIG32, base.image_enclave_config, base.image_enclave_config32, winnt/IMAGE_ENCLAVE_CONFIG32, winnt/PIMAGE_ENCLAVE_CONFIG32'
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
req.typenames: IMAGE_ENCLAVE_CONFIG64, *PIMAGE_ENCLAVE_CONFIG64
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IMAGE_ENCLAVE_CONFIG64
 - winnt/_IMAGE_ENCLAVE_CONFIG64
 - PIMAGE_ENCLAVE_CONFIG64
 - winnt/PIMAGE_ENCLAVE_CONFIG64
 - IMAGE_ENCLAVE_CONFIG64
 - winnt/IMAGE_ENCLAVE_CONFIG64
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
 - IMAGE_ENCLAVE_CONFIG32
 - IMAGE_ENCLAVE_CONFIG
---

# IMAGE_ENCLAVE_CONFIG64 structure


## -description

Defines the format of the enclave configuration for systems running 32-bit Windows.

## -struct-fields

### -field Size

The size of the <b>IMAGE_ENCLAVE_CONFIG32</b> structure, in bytes.

### -field MinimumRequiredConfigSize

The minimum size of the <b>IMAGE_ENCLAVE_CONFIG32</b> structure that the image loader must be able to process in order for the enclave to be usable.  This member allows an enclave to inform an earlier version of the image loader that the image loader can safely load the enclave and ignore optional members added to <b>IMAGE_ENCLAVE_CONFIG32</b> for later versions of the enclave. If the size of <b>IMAGE_ENCLAVE_CONFIG32</b> that the image loader can process is less than <b>MinimumRequiredConfigSize</b>, the enclave cannot be run securely.

If <b>MinimumRequiredConfigSize</b> is zero, the minimum size of the <b>IMAGE_ENCLAVE_CONFIG32</b> structure that the image loader must be able to process in order for the enclave to be usable is assumed to be the size of the structure through and including the <b>MinimumRequiredConfigSize</b> member.

### -field PolicyFlags

A flag that indicates whether the enclave permits debugging.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IMAGE_ENCLAVE_POLICY_DEBUGGABLE"></a><a id="image_enclave_policy_debuggable"></a><dl>
<dt><b>IMAGE_ENCLAVE_POLICY_DEBUGGABLE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The enclave permits debugging.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The enclave does not permit debugging.

</td>
</tr>
</table>

### -field NumberOfImports

The number of images in the array of images that the <b>ImportList</b> member points to.

### -field ImportList

The relative virtual address of the array of images that the enclave image may import, with identity information for each image.

### -field ImportEntrySize

The size of each image in the array of images that the <b>ImportList</b> member points to.

### -field FamilyID

The family identifier that the author of the enclave assigned to the enclave.

### -field ImageID

The image identifier that the author of the enclave assigned to the enclave.

### -field ImageVersion

The version number that the author of the enclave assigned to the enclave.

### -field SecurityVersion

The security version number that the author of the enclave assigned to the enclave.

### -field EnclaveSize

The expected virtual size of the private address range for the enclave, in bytes.

### -field NumberOfThreads

The maximum number of threads that can be created within the enclave.

### -field EnclaveFlags

A flag that indicates whether the image is suitable for use as the primary image in the enclave. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IMAGE_ENCLAVE_FLAG_PRIMARY_IMAGE"></a><a id="image_enclave_flag_primary_image"></a><dl>
<dt><b>IMAGE_ENCLAVE_FLAG_PRIMARY_IMAGE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The image is suitable for use as the primary image in the enclave.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The image is not suitable for use as the primary image in the enclave.

</td>
</tr>
</table>

## -remarks

The <b>IMAGE_ENCLAVE_CONFIG</b> structure is defined as another name for the <b>IMAGE_ENCLAVE_CONFIG32</b> structure on systems that run 32-bit Windows.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/mt844244(v=vs.85)">IMAGE_ENCLAVE_CONFIG64</a>
