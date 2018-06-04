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

# SpSetExtendedInformationFn callback function


## -description


Sets extended information about the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>.


## -parameters




### -param Class [in]

A 
<a href="https://msdn.microsoft.com/52c24886-ae81-4ac8-97d5-d638016e82bf">SECPKG_EXTENDED_INFORMATION_CLASS</a> enumeration value indicating the type of extended information.


### -param Info [in]

Pointer to a 
<a href="https://msdn.microsoft.com/3d80dfc0-c35b-4d14-8196-02944c3db8d2">SECPKG_EXTENDED_INFORMATION</a> structure containing the extended information set.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.




## -remarks



To retrieve extended information, the 
<a href="https://msdn.microsoft.com/e3cb602a-2c98-4e9c-bfbc-f12f353ce3e3">SpGetExtendedInformation</a> function is called.

An SSP/AP must implement the <b>SpSetExtendedInformation</b> function; however, the actual name given to the implementation is up to the package developer.

A pointer to the <b>SpSetExtendedInformation</b> function is available in the 
<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/3d80dfc0-c35b-4d14-8196-02944c3db8d2">SECPKG_EXTENDED_INFORMATION</a>



<a href="https://msdn.microsoft.com/52c24886-ae81-4ac8-97d5-d638016e82bf">SECPKG_EXTENDED_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/d0bff3d8-63f1-4a4e-851f-177040af6bd2">SecPkgInfo</a>



<a href="https://msdn.microsoft.com/e3cb602a-2c98-4e9c-bfbc-f12f353ce3e3">SpGetExtendedInformation</a>



<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a>
 

 

