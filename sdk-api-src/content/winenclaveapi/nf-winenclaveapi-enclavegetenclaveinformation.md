---
UID: NF:winenclaveapi.EnclaveGetEnclaveInformation
title: EnclaveGetEnclaveInformation function
author: windows-sdk-content
description: Gets information about the currently executing enclave.
old-location: base\enclavegetenclaveinformation.htm
tech.root: memory
ms.assetid: 26349C3C-4B73-430C-B002-ED262DB0304F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EnclaveGetEnclaveInformation, EnclaveGetEnclaveInformation function, base.enclavegetenclaveinformation, winenclaveapi/EnclaveGetEnclaveInformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winenclaveapi.h
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
req.lib: Vertdll.lib
req.dll: Vertdll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - vertdll.dll
api_name:
 - EnclaveGetEnclaveInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

