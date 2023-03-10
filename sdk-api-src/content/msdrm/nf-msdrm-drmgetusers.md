---
UID: NF:msdrm.DRMGetUsers
title: DRMGetUsers function (msdrm.h)
description: Retrieves a specific user from an issuance license.
helpviewer_keywords: ["DRMGetUsers","DRMGetUsers function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetUsers","rm.drmgetusers"]
old-location: rm\drmgetusers.htm
tech.root: rm
ms.assetid: 4c8c8249-2e90-4eea-9a3b-dd7d9970ba98
ms.date: 12/05/2018
ms.keywords: DRMGetUsers, DRMGetUsers function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetUsers, rm.drmgetusers
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
 - DRMGetUsers
 - msdrm/DRMGetUsers
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
 - DRMGetUsers
---

# DRMGetUsers function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetUsers</b> function retrieves a specific user from an issuance license.

## -parameters

### -param hIssuanceLicense [in]

The handle of the issuance license to retrieve the user from.

### -param uIndex [in]

The zero-based index of the user in the issuance license to retrieve. To enumerate all the users in the issuance license, create a loop starting at zero and incrementing by one. When the function returns <b>E_DRM_NO_MORE_DATA</b>, there are no more users in the issuance license.

### -param phUser [out]

A pointer to a <b>DRMPUBHANDLE</b> value that receives the handle to the requested user. Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosepubhandle">DRMClosePubHandle</a> to close the handle.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

To enumerate all the users in the issuance license, create a loop starting at zero and incrementing by one. When the function returns <b>E_DRM_NO_MORE_DATA</b>, there are no more users in the issuance license.  Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosepubhandle">DRMClosePubHandle</a> to close the user handle created by calling this function.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetuserinfo">DRMGetUserInfo</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetuserrights">DRMGetUserRights</a>