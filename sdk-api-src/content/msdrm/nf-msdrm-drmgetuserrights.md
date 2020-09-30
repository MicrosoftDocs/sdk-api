---
UID: NF:msdrm.DRMGetUserRights
title: DRMGetUserRights function (msdrm.h)
description: Retrieves user/right pairs from an issuance license.
helpviewer_keywords: ["DRMGetUserRights","DRMGetUserRights function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetUserRights","rm.drmgetuserrights"]
old-location: rm\drmgetuserrights.htm
tech.root: rm
ms.assetid: 46191a8e-66e1-44a5-8052-a21fda88625a
ms.date: 12/05/2018
ms.keywords: DRMGetUserRights, DRMGetUserRights function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetUserRights, rm.drmgetuserrights
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
 - DRMGetUserRights
 - msdrm/DRMGetUserRights
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
 - DRMGetUserRights
---

# DRMGetUserRights function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetUserRights</b> function retrieves user/right pairs from an issuance license.

## -parameters

### -param hIssuanceLicense [in]

The handle of the issuance license to retrieve the user rights from.

### -param hUser [in]

The handle of a user in the issuance license to retrieve the rights for.

### -param uIndex [in]

The zero-based index that indicates which right to retrieve for the specified user. To enumerate all the rights assigned to a user in the issuance license, create a loop starting at zero and incrementing by one. When the function returns <b>E_DRM_NO_MORE_DATA</b>, there are no more rights assigned to that user.

### -param phRight [out]

A pointer to a <b>DRMPUBHANDLE</b> value that receives the handle to the requested right. Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosepubhandle">DRMClosePubHandle</a> to close the handle.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This function gets a right associated with a specific user. User rights are added by using the function <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmaddrightwithuser">DRMAddRightWithUser</a>. To enumerate all rights assigned to a user, pass in a user handle and an index value of zero. Continue to call this function, incrementing the index number by one each time, until <b>E_DRM_NO_MORE_DATA</b> is returned.

Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosepubhandle">DRMClosePubHandle</a> to close the handle created by calling this function.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmaddrightwithuser">DRMAddRightWithUser</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetusers">DRMGetUsers</a>