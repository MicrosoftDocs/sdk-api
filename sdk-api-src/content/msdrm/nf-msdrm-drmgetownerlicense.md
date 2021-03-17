---
UID: NF:msdrm.DRMGetOwnerLicense
title: DRMGetOwnerLicense function (msdrm.h)
description: Retrieves an owner license created by calling the DRMGetSignedIssuanceLicense.
helpviewer_keywords: ["DRMGetOwnerLicense","DRMGetOwnerLicense function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetOwnerLicense","rm.drmgetownerlicense"]
old-location: rm\drmgetownerlicense.htm
tech.root: rm
ms.assetid: e657ac08-9635-40ac-8d9f-cc8ab9ed3a6c
ms.date: 12/05/2018
ms.keywords: DRMGetOwnerLicense, DRMGetOwnerLicense function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetOwnerLicense, rm.drmgetownerlicense
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
 - DRMGetOwnerLicense
 - msdrm/DRMGetOwnerLicense
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
 - DRMGetOwnerLicense
---

# DRMGetOwnerLicense function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetOwnerLicense</b> function retrieves an owner license created by calling the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetsignedissuancelicense">DRMGetSignedIssuanceLicense</a>.

## -parameters

### -param hIssuanceLicense [in]

A handle to a signed issuance license.

### -param puOwnerLicenseLength [in, out]

An unsigned integer that contains the length, in characters, of the owner license retrieved by this function. The terminating null character is included in the length.

### -param wszOwnerLicense [out]

A null-terminated string that contains the owner license in XrML format. For example XrML owner license, see <a href="/previous-versions/windows/desktop/adrms_sdk/owner-license-xml-example">Owner License XML Example</a>.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

An owner license is an end-user license that contains the OWNER right and allows the user to exercise all rights regardless of whether they are specifically granted. It is created by the AD RMS client when you call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetsignedissuancelicense">DRMGetSignedIssuanceLicense</a> and sign an issuance license offline.  If <b>DRMGetSignedIssuanceLicense</b> is called with the <i>uFlags</i> parameter set to <b>DRM_OWNER_LICENSE_NOPERSIST</b>, the owner license is saved in memory. Otherwise, it is saved in the license store. The <b>DRMGetOwnerLicense</b> function automatically retrieves the license from either location.

## -see-also

<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetsignedissuancelicense">DRMGetSignedIssuanceLicense</a>