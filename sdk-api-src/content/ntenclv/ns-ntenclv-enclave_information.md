---
UID: NS:ntenclv.ENCLAVE_INFORMATION
title: ENCLAVE_INFORMATION (ntenclv.h)
description: Contains information about the currently executing enclave.helpviewer_keywords: ["ENCLAVE_INFORMATION","ENCLAVE_INFORMATION structure","ENCLAVE_TYPE_SGX","ENCLAVE_TYPE_VBS","base.enclave_information","ntenclv/ENCLAVE_INFORMATION"]
old-location: base\enclave_information.htm
tech.root: Memory
ms.assetid: 6720EDBE-6A0E-4192-A096-2ACA681E2AAF
ms.date: 12/05/2018
ms.keywords: ENCLAVE_INFORMATION, ENCLAVE_INFORMATION structure, ENCLAVE_TYPE_SGX, ENCLAVE_TYPE_VBS, base.enclave_information, ntenclv/ENCLAVE_INFORMATION
f1_keywords:
- ntenclv/ENCLAVE_INFORMATION
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- ntenclv.h
api_name:
- ENCLAVE_INFORMATION
targetos: Windows
req.typenames: ENCLAVE_INFORMATION
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/ntenclv/ns-ntenclv-enclave_identity">ENCLAVE_IDENTITY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetenclaveinformation">EnclaveGetEnclaveInformation</a>
 

 

