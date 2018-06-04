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

# _ENCLAVE_CREATE_INFO_SGX structure


## -description


Contains architecture-specific information to use to create an enclave when the enclave type is <b>ENCLAVE_TYPE_SGX</b>, which specifies an enclave for the Intel Software Guard Extensions (SGX) architecture extension.


## -struct-fields




### -field Secs

The SGX enclave control structure (<b>SECS</b>) to use to create the enclave.


## -remarks



For more information about the <b>SECS</b> structure, see the Intel SGX Programming Reference that is available from <a href="https://go.microsoft.com/fwlink/p/?linkid=691175">Intel Software Guard Extensions</a>.




## -see-also




<a href="https://msdn.microsoft.com/2193AE42-D9CC-4A9C-8676-7DE432ED58C3">CreateEnclave</a>



<a href="https://msdn.microsoft.com/A314FF96-A212-4F47-B836-224DE2C3AC0F">ENCLAVE_INIT_INFO_SGX</a>
 

 

