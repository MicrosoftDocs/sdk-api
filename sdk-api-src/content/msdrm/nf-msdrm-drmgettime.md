---
UID: NF:msdrm.DRMGetTime
title: DRMGetTime function (msdrm.h)
description: Requests a secure time from the rights management system.
helpviewer_keywords: ["DRMGetTime","DRMGetTime function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetTime","rm.drmgettime"]
old-location: rm\drmgettime.htm
tech.root: rm
ms.assetid: 124507af-ccb4-4552-9421-bbbf1b556930
ms.date: 12/05/2018
ms.keywords: DRMGetTime, DRMGetTime function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetTime, rm.drmgettime
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
req.product: Rights Management Services client 1.0 SP2  or later
ms.custom: 19H1
f1_keywords:
 - DRMGetTime
 - msdrm/DRMGetTime
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
 - DRMGetTime
---

# DRMGetTime function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetTime</b> function requests a secure time from the rights management system.

## -parameters

### -param hEnv [in]

Environment handle.

### -param eTimerIdType [in]

The type of time returned.

### -param poTimeObject [out]

Pointer to a time structure.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>