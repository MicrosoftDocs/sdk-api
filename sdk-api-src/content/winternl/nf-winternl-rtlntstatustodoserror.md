---
UID: NF:winternl.RtlNtStatusToDosError
title: RtlNtStatusToDosError function (winternl.h)
description: Converts the specified NTSTATUS code to its equivalent system error code.
helpviewer_keywords: ["RtlNtStatusToDosError","RtlNtStatusToDosError function","base.rtlntstatustodoserror","winternl/RtlNtStatusToDosError"]
old-location: base\rtlntstatustodoserror.htm
tech.root: Debug
ms.assetid: 4a28be1f-28b9-45a4-8ac7-58e43452558a
ms.date: 12/05/2018
ms.keywords: RtlNtStatusToDosError, RtlNtStatusToDosError function, base.rtlntstatustodoserror, winternl/RtlNtStatusToDosError
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
req.lib: ntdll.lib
req.dll: ntdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtlNtStatusToDosError
 - winternl/RtlNtStatusToDosError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
api_name:
 - RtlNtStatusToDosError
---

# RtlNtStatusToDosError function


## -description

Converts the specified NTSTATUS code to its equivalent system error code.

## -parameters

### -param Status [in]

The NTSTATUS code to be converted.

## -returns

The function returns the corresponding <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

There is no function that provides the inverse functionality of <b>RtlNtStatusToDosError</b>, which would convert a system error code to its corresponding NTSTATUS code.

ERROR_MR_MID_NOT_FOUND is returned when the specified NTSTATUS code does not have a corresponding system error code.

## -see-also

<a href="/windows/desktop/Debug/error-handling-functions">Error Handling Functions</a>
