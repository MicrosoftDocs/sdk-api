---
UID: NF:msdrm.DRMDuplicateSession
title: DRMDuplicateSession function (msdrm.h)
description: Duplicates a client or license storage session.
helpviewer_keywords: ["DRMDuplicateSession","DRMDuplicateSession function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMDuplicateSession","rm.drmduplicatesession"]
old-location: rm\drmduplicatesession.htm
tech.root: rm
ms.assetid: 4a768919-36aa-4e09-898f-bd8f9c21cb0e
ms.date: 12/05/2018
ms.keywords: DRMDuplicateSession, DRMDuplicateSession function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMDuplicateSession, rm.drmduplicatesession
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
 - DRMDuplicateSession
 - msdrm/DRMDuplicateSession
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
 - DRMDuplicateSession
---

# DRMDuplicateSession function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMDuplicateSession</b> function duplicates a client or license storage session.

## -parameters

### -param hSessionIn [in]

A handle to a session to duplicate.

### -param phSessionOut [out]

Pointer to the duplicated session handle. Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosesession">DRMCloseSession</a> to close the handle.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Creating, copying, and closing handles with the appropriate function allows the rights management system to maintain a reference count on resources and free them appropriately, and also clears sensitive data from memory. Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosesession">DRMCloseSession</a> to close the handle created by calling this function.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>