---
UID: NF:msdrm.DRMDuplicateHandle
title: DRMDuplicateHandle function (msdrm.h)
author: windows-sdk-content
description: Creates a copy of a DRMHANDLE.
old-location: rm\drmduplicatehandle.htm
tech.root: AdRms_Sdk
ms.assetid: 967519da-0471-4615-aec0-b30717239dd5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DRMDuplicateHandle, DRMDuplicateHandle function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMDuplicateHandle, rm.drmduplicatehandle
ms.topic: function
f1_keywords: 
 - "msdrm/DRMDuplicateHandle"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMDuplicateHandle
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
---

# DRMDuplicateHandle function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://docs.microsoft.com/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMDuplicateHandle</b> function creates a copy of a <b>DRMHANDLE</b>.


## -parameters




### -param hToCopy [in]

A handle to copy.


### -param phCopy [out]

A copy of the handle. Call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosehandle">DRMCloseHandle</a> to close the handle.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -remarks



Use this function to duplicate all handles except environment handles. (For that, use <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmduplicateenvironmenthandle">DRMDuplicateEnvironmentHandle</a>.) This function allows an application to keep a proper reference count on environment handles. Call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosehandle">DRMCloseHandle</a> to close the handle created by calling this function.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>
 

 

