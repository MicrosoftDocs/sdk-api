---
UID: NF:msdrm.DRMCheckSecurity
title: DRMCheckSecurity function (msdrm.h)
description: Returns S_OK for any level of the security check being run.
helpviewer_keywords: ["DRMCheckSecurity","DRMCheckSecurity function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMCheckSecurity","rm.drmchecksecurity"]
old-location: rm\drmchecksecurity.htm
tech.root: rm
ms.assetid: 8c0ea50b-ba7c-4cbc-9e1d-4089995374f8
ms.date: 12/05/2018
ms.keywords: DRMCheckSecurity, DRMCheckSecurity function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCheckSecurity, rm.drmchecksecurity
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
 - DRMCheckSecurity
 - msdrm/DRMCheckSecurity
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
 - DRMCheckSecurity
---

# DRMCheckSecurity function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

In the Rights Management Services client 1.0 SP1 and later versions, the <b>DRMCheckSecurity</b> function returns <b>S_OK</b> for any level of the security check being run.

## -parameters

### -param hEnv [in]

A handle to an environment.

### -param cLevel [in]

Level of the security check to run, from 1 to 10, with 10 being the most secure but most resource-intensive.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Currently only environment security checks are allowed. A comprehensive security check can be time-consuming.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>