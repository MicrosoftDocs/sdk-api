---
UID: NF:msdrm.DRMCloseHandle
title: DRMCloseHandle function (msdrm.h)
description: Closes handles to objects created with DRMCreate* functions and libraries loaded by using DRMLoadLibrary.
helpviewer_keywords: ["DRMCloseHandle","DRMCloseHandle function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMCloseHandle","rm.drmclosehandle"]
old-location: rm\drmclosehandle.htm
tech.root: rm
ms.assetid: 422f286c-edf6-488f-8776-359ab2695be3
ms.date: 12/05/2018
ms.keywords: DRMCloseHandle, DRMCloseHandle function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCloseHandle, rm.drmclosehandle
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
 - DRMCloseHandle
 - msdrm/DRMCloseHandle
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
 - DRMCloseHandle
---

# DRMCloseHandle function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCloseHandle</b> function closes handles to objects created with <b>DRMCreate</b>* functions and libraries loaded by using <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmloadlibrary">DRMLoadLibrary</a>.

## -parameters

### -param handle [in]

A handle to close.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This function properly clears sensitive data from memory and allows the AD RMS system to keep an accurate reference count on objects used. If an object contains other open objects within it, calling this function will force all contained objects to be closed as well. However, forcing closure of contained objects in this way is not recommended.

If this function fails, an application should destroy the current process after closing the environment with <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcloseenvironmenthandle">DRMCloseEnvironmentHandle</a>.

Closing a handle to a library will cause the library to be unloaded if it has no remaining open objects.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-handles-and-sessions">AD RMS Handles and Sessions</a>