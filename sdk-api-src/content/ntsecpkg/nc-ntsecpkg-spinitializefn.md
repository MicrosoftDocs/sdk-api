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

# SpInitializeFn callback function


## -description


The <b>SpInitialize</b> function is called once by the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA) to provide a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> with general security information and a dispatch table of support functions. The security package should save the information and do internal initialization processing, if any is needed.


## -parameters




### -param PackageId [in]

A unique identifier the LSA assigns to each security package. The value is valid until the system is restarted.


### -param Parameters [in]

A pointer to a 
<a href="https://msdn.microsoft.com/2e3b7961-e2c4-4011-91b1-0ba9d35e9188">SECPKG_PARAMETERS</a> structure containing primary domain and machine state information.


### -param FunctionTable [in]

Pointer to a table of LSA support functions that a security package can call.


## -returns



If the function succeeds, return STATUS_SUCCESS, or an informational status code.

If the function fails, return an NTSTATUS error code indicating the reason it failed. For more information, see Remarks.




## -remarks



If <b>SpInitialize</b> returns an NTSTATUS error code to the LSA, the package will be unloaded, and the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA) will not include it in the list of available security packages.

SSP/APs must implement the <b>SpInitialize</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the SSP/AP's implementation of the <b>SpInitialize</b> function must be in the 
<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a> structure passed to the LSA from the 
<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/2e3b7961-e2c4-4011-91b1-0ba9d35e9188">SECPKG_PARAMETERS</a>



<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a>
 

 

