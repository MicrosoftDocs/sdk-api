---
UID: NF:winternl.RtlNtStatusToDosError
title: RtlNtStatusToDosError function (winternl.h)
author: windows-sdk-content
description: Converts the specified NTSTATUS code to its equivalent system error code.
old-location: base\rtlntstatustodoserror.htm
tech.root: Debug
ms.assetid: 4a28be1f-28b9-45a4-8ac7-58e43452558a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RtlNtStatusToDosError, RtlNtStatusToDosError function, base.rtlntstatustodoserror, winternl/RtlNtStatusToDosError
ms.topic: function
req.header: winternl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Ntdll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
api_name:
 - RtlNtStatusToDosError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtlNtStatusToDosError function


## -description


Converts the specified NTSTATUS code to its equivalent system error code.


## -parameters




### -param Status [in]

The NTSTATUS code to be converted.


## -returns



The function returns the corresponding <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



There is no function that provides the inverse functionality of <b>RtlNtStatusToDosError</b>, which would convert a system error code to its corresponding NTSTATUS code.

ERROR_MR_MID_NOT_FOUND is returned when the specified NTSTATUS code does not have a corresponding system error code.

This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Ntdll.dll.




## -see-also




<a href="https://msdn.microsoft.com/ae8ad3a2-1f1a-46d6-adaa-74c50c07dcc5">Error Handling Functions</a>
 

 

