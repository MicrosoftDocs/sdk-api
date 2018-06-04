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

# EnclaveVerifyAttestationReport function


## -description


Verifies an attestation report that was generated on the current system. 


## -parameters




### -param EnclaveType [in]

The type of the enclave for which the report was generated. Must be <b>ENCLAVE_TYPE_VBS</b>.


### -param Report [in]

A pointer to a buffer that stores the report.  This report may be stored either within the address range of the enclave or within the address space of the host process.


### -param ReportSize [in]

 The size of the report, in bytes.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is used if two enclaves run on the same system and need to establish a secure channel between one another.  When you call <b>EnclaveVerifyAttestationReport</b> from a virtualization-based security (VBS) enclave, you can only use <b>EnclaveVerifyAttestationReport</b> to validate an attestation report that another VBS enclave generated.

<b>EnclaveVerifyAttestationReport</b> must be called from within an enclave, and is only supported within enclaves that have the  <b>ENCLAVE_TYPE_VBS</b> enclave type.




## -see-also




<a href="https://msdn.microsoft.com/FEE8F05B-540F-4C10-A90C-55607A4E9293">EnclaveGetAttestationReport</a>
 

 

