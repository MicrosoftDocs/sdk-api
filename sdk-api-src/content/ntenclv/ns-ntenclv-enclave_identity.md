---
UID: NS:ntenclv.ENCLAVE_IDENTITY
title: ENCLAVE_IDENTITY
author: windows-sdk-content
description: Describes the identity of the primary module of an enclave.
old-location: base\enclave_identity.htm
old-project: Memory
ms.assetid: D584D824-3C86-4BBB-9086-6DBE0290E0A4
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ENCLAVE_FLAG_DYNAMIC_DEBUG_ACTIVE, ENCLAVE_FLAG_DYNAMIC_DEBUG_ENABLED, ENCLAVE_FLAG_FULL_DEBUG_ENABLED, ENCLAVE_IDENTITY, ENCLAVE_IDENTITY structure, base.enclave_identity, ntenclv/ENCLAVE_IDENTITY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntenclv.h
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
req.typenames: ENCLAVE_IDENTITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ntenclv.h
api_name:
-	ENCLAVE_IDENTITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

