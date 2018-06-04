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

# ENCLAVE_IDENTITY structure


## -description


Describes the identity of the primary module of an enclave. 


## -struct-fields




### -field OwnerId

The identifier of the owner for the enclave. 


### -field UniqueId

The unique identifier of the primary module for the enclave.


### -field AuthorId

The author identifier of the primary module for the enclave.


### -field FamilyId

The family identifier of the primary module for the enclave.


### -field ImageId

The image identifier of the primary module for the enclave.


### -field EnclaveSvn

The security version number of the primary module for the enclave.


### -field SecureKernelSvn

The security version number of the Virtual Secure Mode (VSM) kernel.


### -field PlatformSvn

The security version number of the platform that hosts the enclave.


### -field Flags

Flags that describe the runtime policy for the enclave.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ENCLAVE_FLAG_FULL_DEBUG_ENABLED"></a><a id="enclave_flag_full_debug_enabled"></a><dl>
<dt><b>ENCLAVE_FLAG_FULL_DEBUG_ENABLED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The enclave supports debugging.

</td>
</tr>
<tr>
<td width="40%"><a id="ENCLAVE_FLAG_DYNAMIC_DEBUG_ENABLED"></a><a id="enclave_flag_dynamic_debug_enabled"></a><dl>
<dt><b>ENCLAVE_FLAG_DYNAMIC_DEBUG_ENABLED</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The enclave supports dynamic debugging.

</td>
</tr>
<tr>
<td width="40%"><a id="ENCLAVE_FLAG_DYNAMIC_DEBUG_ACTIVE"></a><a id="enclave_flag_dynamic_debug_active"></a><dl>
<dt><b>ENCLAVE_FLAG_DYNAMIC_DEBUG_ACTIVE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Dynamic debugging is turned on for the enclave.

</td>
</tr>
</table>
 


### -field SigningLevel

The signing level of the primary module for the enclave.


### -field Reserved

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/90D6E8D2-191B-41D2-8C75-28A26462644B">VBS_ENCLAVE_REPORT</a>
 

 

