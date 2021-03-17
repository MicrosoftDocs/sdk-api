---
UID: NF:msdrm.DRMDuplicatePubHandle
title: DRMDuplicatePubHandle function (msdrm.h)
description: Makes a copy of a DRMPUBHANDLE.
helpviewer_keywords: ["DRMDuplicatePubHandle","DRMDuplicatePubHandle function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMDuplicatePubHandle","rm.drmduplicatepubhandle"]
old-location: rm\drmduplicatepubhandle.htm
tech.root: rm
ms.assetid: 6bf94d17-ce09-492e-9b47-88cd54719d3e
ms.date: 12/05/2018
ms.keywords: DRMDuplicatePubHandle, DRMDuplicatePubHandle function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMDuplicatePubHandle, rm.drmduplicatepubhandle
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
 - DRMDuplicatePubHandle
 - msdrm/DRMDuplicatePubHandle
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
 - DRMDuplicatePubHandle
---

# DRMDuplicatePubHandle function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMDuplicatePubHandle</b> function makes a copy of a <b>DRMPUBHANDLE</b>.

## -parameters

### -param hPubIn [in]

The <b>DRMPUBHANDLE</b> to make a copy of.

### -param phPubOut [out]

A pointer to a <b>DRMPUBHANDLE</b> value that receives the duplicate handle. When this handle is no longer needed, release it  by passing it to the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosepubhandle">DRMClosePubHandle</a> function.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Using the appropriate function to create, copy, and close these handles allows Active Directory Rights Management Services to maintain a reference count on resources and free them appropriately; it also clears sensitive data from memory.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosepubhandle">DRMClosePubHandle</a>