---
UID: NF:msdrm.DRMDuplicateEnvironmentHandle
title: DRMDuplicateEnvironmentHandle function (msdrm.h)
description: Creates a copy of an environment handle.
helpviewer_keywords: ["DRMDuplicateEnvironmentHandle","DRMDuplicateEnvironmentHandle function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMDuplicateEnvironmentHandle","rm.drmduplicateenvironmenthandle"]
old-location: rm\drmduplicateenvironmenthandle.htm
tech.root: rm
ms.assetid: 6e246181-1d93-49b4-bc3f-e54083d4cad2
ms.date: 12/05/2018
ms.keywords: DRMDuplicateEnvironmentHandle, DRMDuplicateEnvironmentHandle function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMDuplicateEnvironmentHandle, rm.drmduplicateenvironmenthandle
req.header: msdrm.h
req.include-header: 
req.target-type: Windows
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
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - DRMDuplicateEnvironmentHandle
 - msdrm/DRMDuplicateEnvironmentHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMDuplicateEnvironmentHandle
---

# DRMDuplicateEnvironmentHandle function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMDuplicateEnvironmentHandle</b> function creates a copy of an environment handle.

## -parameters

### -param hToCopy [in]

A handle to copy. An environment handle is created by using <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drminitenvironment">DRMInitEnvironment</a>.

### -param phCopy [out]

A copy of the handle. Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcloseenvironmenthandle">DRMCloseEnvironmentHandle</a> to close.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This function allows an application to keep a proper reference count on environment handles, so use this function, rather than simply copy assignment, to copy an environment handle. For other handles, use <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmduplicatehandle">DRMDuplicateHandle</a>. Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcloseenvironmenthandle">DRMCloseEnvironmentHandle</a> to close the environment handle created by calling this function.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>