---
UID: NF:msdrm.DRMClearAllRights
title: DRMClearAllRights function (msdrm.h)
description: Removes all rights from an existing issuance license.
helpviewer_keywords: ["DRMClearAllRights","DRMClearAllRights function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMClearAllRights","rm.drmclearallrights"]
old-location: rm\drmclearallrights.htm
tech.root: rm
ms.assetid: f0a5dc8d-2bc6-4fcc-8871-ea80fc6a4abc
ms.date: 12/05/2018
ms.keywords: DRMClearAllRights, DRMClearAllRights function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMClearAllRights, rm.drmclearallrights
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
 - DRMClearAllRights
 - msdrm/DRMClearAllRights
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
 - DRMClearAllRights
---

# DRMClearAllRights function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMClearAllRights</b> function removes all rights from an existing issuance license.

## -parameters

### -param hIssuanceLicense [in]

A handle to the issuance license to remove the rights from.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

There is no way to remove individual rights from an issuance license.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmaddrightwithuser">DRMAddRightWithUser</a>