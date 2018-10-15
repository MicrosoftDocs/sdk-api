---
UID: NF:ntsecapi.LsaNtStatusToWinError
title: LsaNtStatusToWinError function
author: windows-sdk-content
description: The LsaNtStatusToWinError function converts an NTSTATUS code returned by an LSA function to a Windows error code.
old-location: security\lsantstatustowinerror.htm
tech.root: secmgmt
ms.assetid: fa91794c-c502-4b36-84cc-a8d77c8e9d9f
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: LsaNtStatusToWinError, LsaNtStatusToWinError function [Security], _lsa_lsantstatustowinerror, ntsecapi/LsaNtStatusToWinError, security.lsantstatustowinerror
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntsecapi.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - Secur32.dll
api_name:
 - LsaNtStatusToWinError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LsaNtStatusToWinError function


## -description


The <b>LsaNtStatusToWinError</b> function converts an NTSTATUS code returned by an LSA function to a Windows error code.


## -parameters




### -param Status [in]

An NTSTATUS code returned by an LSA function call. This value will be converted to a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System error code</a>.


## -returns



The return value is the Windows error code that corresponds to the <i>Status</i> parameter. If there is no corresponding Windows error code, the return value is ERROR_MR_MID_NOT_FOUND.




## -see-also




<a href="management_return_values.htm">LSA Policy Function Return Values</a>
 

 

