---
UID: NF:ntsecapi.LsaNtStatusToWinError
title: LsaNtStatusToWinError function (ntsecapi.h)
description: The LsaNtStatusToWinError function converts an NTSTATUS code returned by an LSA function to a Windows error code.
helpviewer_keywords: ["LsaNtStatusToWinError","LsaNtStatusToWinError function [Security]","_lsa_lsantstatustowinerror","ntsecapi/LsaNtStatusToWinError","security.lsantstatustowinerror"]
old-location: security\lsantstatustowinerror.htm
tech.root: security
ms.assetid: fa91794c-c502-4b36-84cc-a8d77c8e9d9f
ms.date: 12/05/2018
ms.keywords: LsaNtStatusToWinError, LsaNtStatusToWinError function [Security], _lsa_lsantstatustowinerror, ntsecapi/LsaNtStatusToWinError, security.lsantstatustowinerror
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LsaNtStatusToWinError
 - ntsecapi/LsaNtStatusToWinError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-advapi32-lsa-l1-1-4.dll
 - ext-ms-win-advapi32-lsa-l1-1-3.dll
 - ext-ms-win-advapi32-lsa-l1-1-2.dll
 - Advapi32.dll
 - Secur32.dll
api_name:
 - LsaNtStatusToWinError
---

# LsaNtStatusToWinError function


## -description

The <b>LsaNtStatusToWinError</b> function converts an NTSTATUS code returned by an LSA function to a Windows error code.

## -parameters

### -param Status [in]

An NTSTATUS code returned by an LSA function call. This value will be converted to a 
<a href="/windows/desktop/Debug/system-error-codes">System error code</a>.

## -returns

The return value is the Windows error code that corresponds to the <i>Status</i> parameter. If there is no corresponding Windows error code, the return value is ERROR_MR_MID_NOT_FOUND.

## -see-also

<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>