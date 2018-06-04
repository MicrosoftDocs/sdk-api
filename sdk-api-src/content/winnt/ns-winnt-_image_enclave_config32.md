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

# _IMAGE_ENCLAVE_CONFIG32 structure


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




<a href="https://msdn.microsoft.com/D76F7868-910B-4DC4-939A-6376802E170D">IMAGE_ENCLAVE_CONFIG64</a>
 

 

