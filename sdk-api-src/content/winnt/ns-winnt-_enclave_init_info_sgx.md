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

# _ENCLAVE_INIT_INFO_SGX structure


## -description


Contains architecture-specific information to use to initialize an enclave when the enclave type is <b>ENCLAVE_TYPE_SGX</b>, which specifies an enclave for the Intel Software Guard Extensions (SGX) architecture extension.


## -struct-fields




### -field SigStruct

The enclave signature structure (<b>SIGSTRUCT</b>) to use  to initialize the enclave. This structure specifies information about the enclave from the enclave signer.


### -field Reserved1

Not used.


### -field EInitToken

The EINIT token structure (<b>EINITTOKEN</b>) to use  to initialize the enclave. The initialization operation uses this structure to verify that the enclave has permission to start.


### -field Reserved2

Not used.


## -remarks



For more information about the <b>SIGSTRUCT</b> and <b>EINITTOKEN</b> structures, see the Intel SGX Programming Reference that is available from <a href="https://go.microsoft.com/fwlink/p/?linkid=691175">Intel Software Guard Extensions</a>.




## -see-also




<a href="https://msdn.microsoft.com/51ED6E75-DA18-4CCE-8718-46328DD62B07">ENCLAVE_CREATE_INFO_SGX</a>



<a href="https://msdn.microsoft.com/6A711135-A522-40AE-965F-E1AF97D0076A">InitializeEnclave</a>
 

 

