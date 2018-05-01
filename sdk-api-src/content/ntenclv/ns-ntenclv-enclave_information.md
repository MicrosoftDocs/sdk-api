---
UID: NS:ntenclv.ENCLAVE_INFORMATION
title: ENCLAVE_INFORMATION
author: windows-driver-content
description: Contains information about the currently executing enclave.
old-location: base\enclave_information.htm
old-project: Memory
ms.assetid: 6720EDBE-6A0E-4192-A096-2ACA681E2AAF
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: ENCLAVE_INFORMATION, ENCLAVE_INFORMATION structure, ENCLAVE_TYPE_SGX, ENCLAVE_TYPE_VBS, base.enclave_information, ntenclv/ENCLAVE_INFORMATION
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: ENCLAVE_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ntenclv.h
api_name:
-	ENCLAVE_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ENCLAVE_INFORMATION structure


## -description


Contains information about the currently executing enclave.


## -struct-fields




### -field EnclaveType

The architecture type of the enclave.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ENCLAVE_TYPE_SGX"></a><a id="enclave_type_sgx"></a><dl>
<dt><b><b>ENCLAVE_TYPE_SGX</b></b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
An enclave for the Intel Software Guard Extensions (SGX) architecture extension.

</td>
</tr>
<tr>
<td width="40%"><a id="ENCLAVE_TYPE_VBS"></a><a id="enclave_type_vbs"></a><dl>
<dt><b>ENCLAVE_TYPE_VBS</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
A  VBS enclave.

</td>
</tr>
</table>
 


### -field Reserved

Reserved.


### -field BaseAddress

A pointer to the base address of the enclave.


### -field Size

The size of the enclave, in bytes.


### -field Identity

The identity of the primary module of an enclave.


## -see-also




<a href="https://msdn.microsoft.com/D584D824-3C86-4BBB-9086-6DBE0290E0A4">ENCLAVE_IDENTITY</a>



<a href="https://msdn.microsoft.com/26349C3C-4B73-430C-B002-ED262DB0304F">EnclaveGetEnclaveInformation</a>
 

 

