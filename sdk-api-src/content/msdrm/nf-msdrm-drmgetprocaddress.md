---
UID: NF:msdrm.DRMGetProcAddress
title: DRMGetProcAddress function (msdrm.h)
description: Returns the address of a function in a library. It is the secure version of the GetProcAddress function.
helpviewer_keywords: ["DRMGetProcAddress","DRMGetProcAddress function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetProcAddress","rm.drmgetprocaddress"]
old-location: rm\drmgetprocaddress.htm
tech.root: rm
ms.assetid: 4ce2adac-f6d3-4760-984e-08a0d11a30d1
ms.date: 12/05/2018
ms.keywords: DRMGetProcAddress, DRMGetProcAddress function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetProcAddress, rm.drmgetprocaddress
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
 - DRMGetProcAddress
 - msdrm/DRMGetProcAddress
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
 - DRMGetProcAddress
---

# DRMGetProcAddress function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetProcAddress</b> function returns the address of a function in a library. It is the secure version of the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> function.

## -parameters

### -param hLibrary [in]

A handle to the library where the function resides. Output from <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmloadlibrary">DRMLoadLibrary</a> or <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drminitenvironment">DRMInitEnvironment</a>.

### -param wszProcName [in]

The name of the function to find the address of.

### -param ppfnProcAddress [out]

Address of the procedure to run.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

For more information about this function, see <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drminitenvironment">DRMInitEnvironment</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmloadlibrary">DRMLoadLibrary</a>