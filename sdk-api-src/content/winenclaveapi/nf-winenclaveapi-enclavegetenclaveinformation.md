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

# EnclaveGetEnclaveInformation function


## -description


Gets information about the currently executing enclave.


## -parameters




### -param InformationSize [in]

The size of the <a href="https://msdn.microsoft.com/6720EDBE-6A0E-4192-A096-2ACA681E2AAF">ENCLAVE_INFORMATION</a> structure that the <i>EnclaveInformation</i> parameter points to, in bytes.


### -param EnclaveInformation [out]

Information about the currently executing enclave.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>EnclaveGetEnclaveInformation</b> must be called from within an enclave, and is only supported within enclaves that have the  <b>ENCLAVE_TYPE_VBS</b> enclave type.




## -see-also




<a href="https://msdn.microsoft.com/6720EDBE-6A0E-4192-A096-2ACA681E2AAF">ENCLAVE_INFORMATION</a>
 

 

