---
UID: NF:msdrm.DRMCloseQueryHandle
title: DRMCloseQueryHandle function (msdrm.h)
author: windows-sdk-content
description: Closes a handle to an unbound license object.
old-location: rm\drmclosequeryhandle.htm
tech.root: AdRms_Sdk
ms.assetid: 4902a6e2-e3b2-4f05-970c-aa4f80895762
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DRMCloseQueryHandle, DRMCloseQueryHandle function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCloseQueryHandle, rm.drmclosequeryhandle
ms.topic: function
f1_keywords: 
 - "msdrm/DRMCloseQueryHandle"
dev_langs:
 - c++
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
 - DRMCloseQueryHandle
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2  or later
ms.custom: 19H1
---

# DRMCloseQueryHandle function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://docs.microsoft.com/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCloseQueryHandle</b> function closes a handle to an unbound license object.


## -parameters




### -param hQuery [in]

A handle to an object in an unbound license.


## -returns



 If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -remarks



The AD RMS system exposes an object-oriented interface to a license. Bound licenses are accessed using a <b>DRMHANDLE</b>, while unbound licenses are accessed by a <b>DRMQUERYHANDLE</b>. The two types are not interchangeable. This function closes unbound licenses. For more information about examining unbound licenses, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmparseunboundlicense">DRMParseUnboundLicense</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>
 

 

