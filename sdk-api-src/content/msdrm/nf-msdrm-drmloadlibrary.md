---
UID: NF:msdrm.DRMLoadLibrary
title: DRMLoadLibrary function (msdrm.h)
description: Loads a handle to an approved library, as determined by the credentials.
helpviewer_keywords: ["DRMLoadLibrary","DRMLoadLibrary function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMLoadLibrary","rm.drmloadlibrary"]
old-location: rm\drmloadlibrary.htm
tech.root: rm
ms.assetid: b0a95d3f-4252-4685-bc51-547620b5dcf7
ms.date: 12/05/2018
ms.keywords: DRMLoadLibrary, DRMLoadLibrary function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMLoadLibrary, rm.drmloadlibrary
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
 - DRMLoadLibrary
 - msdrm/DRMLoadLibrary
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
 - DRMLoadLibrary
---

# DRMLoadLibrary function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMLoadLibrary</b> function loads a handle to an approved library, as determined by the credentials.

## -parameters

### -param hEnv [in]

A handle to an environment, created by <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drminitenvironment">DRMInitEnvironment</a>.

### -param eSpecification [in]

The library provider type.

### -param wszLibraryProvider [in]

Name and optional path to the DLL. Every DLL must have a unique name. If similarly named DLLs are loaded, even if they are in different paths, only the first item will be included in the manifest and checked.

### -param wszCredentials [in]

Reserved, must be <b>NULL</b>. The DLL that is loaded must be referenced in the application manifest loaded by <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drminitenvironment">DRMInitEnvironment</a>.

### -param phLibrary [out]

A handle to the library.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This function is a secure version of the  <b>LoadLibrary</b> function, however it does not support the extra options of <b>LoadLibraryEx</b>. The returned handle corresponds to the HMODULE output by LoadLibrary. To close the handle returned, call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosehandle">DRMCloseHandle</a>, not <b>FreeLibrary</b>. By default, the current directory is the only location this function searches for a library. Any other directory must be specified by either a full path, or a path relative to the current directory. Use <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetprocaddress">DRMGetProcAddress</a>, the secure version of the <b>GetProcAddress</b> function, to get function addresses in loaded libraries.

Dependencies of the loaded DLL will also be loaded, provided they are included in the plug-in credentials and are properly signed. If the DLL has already been loaded, the function will return S_OK and return a pointer to the same handle.<div class="alert"><b>Note</b>  If an application attempts to load a second library with the name of a previously loaded library, this new library will not be checked against the manifest, even if it is from a different path. Use only uniquely named libraries to avoid this circumvention of manifest checking.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetprocaddress">DRMGetProcAddress</a>