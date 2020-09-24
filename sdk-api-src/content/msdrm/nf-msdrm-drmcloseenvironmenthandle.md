---
UID: NF:msdrm.DRMCloseEnvironmentHandle
title: DRMCloseEnvironmentHandle function (msdrm.h)
description: Closes an environment handle.
helpviewer_keywords: ["DRMCloseEnvironmentHandle","DRMCloseEnvironmentHandle function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMCloseEnvironmentHandle","rm.drmcloseenvironmenthandle"]
old-location: rm\drmcloseenvironmenthandle.htm
tech.root: rm
ms.assetid: 3edde872-a863-4c7f-92f0-f7e324aff651
ms.date: 12/05/2018
ms.keywords: DRMCloseEnvironmentHandle, DRMCloseEnvironmentHandle function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCloseEnvironmentHandle, rm.drmcloseenvironmenthandle
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
 - DRMCloseEnvironmentHandle
 - msdrm/DRMCloseEnvironmentHandle
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
 - DRMCloseEnvironmentHandle
---

# DRMCloseEnvironmentHandle function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCloseEnvironmentHandle</b> function closes an environment handle.

## -parameters

### -param hEnv [in]

A handle to an environment.

## -returns

 If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This function is the last function an application should call in a secure environment. Close embedded handles first by calling <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosehandle">DRMCloseHandle</a>. Calling <b>DRMClose</b>* functions clears out sensitive information from memory and allows the Active Directory Rights Management system to keep an accurate reference count on objects used.

If this function fails, an application should destroy the current process before reinitializing an environment to use.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>