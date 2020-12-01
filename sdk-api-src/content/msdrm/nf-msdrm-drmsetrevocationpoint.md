---
UID: NF:msdrm.DRMSetRevocationPoint
title: DRMSetRevocationPoint function (msdrm.h)
description: Sets a refresh rate and location to obtain a revocation list.
helpviewer_keywords: ["DRMSetRevocationPoint","DRMSetRevocationPoint function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMSetRevocationPoint","rm.drmsetrevocationpoint"]
old-location: rm\drmsetrevocationpoint.htm
tech.root: rm
ms.assetid: a9f4ff8d-1b9f-46f4-8a69-5957d4b2aefb
ms.date: 12/05/2018
ms.keywords: DRMSetRevocationPoint, DRMSetRevocationPoint function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMSetRevocationPoint, rm.drmsetrevocationpoint
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
 - DRMSetRevocationPoint
 - msdrm/DRMSetRevocationPoint
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
 - DRMSetRevocationPoint
---

# DRMSetRevocationPoint function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMSetRevocationPoint</b> function sets a refresh rate and location to obtain a revocation list.

## -parameters

### -param hIssuanceLicense [in]

A handle to an issuance license.

### -param fDelete [in]

Flag indicating whether the existing item should be deleted:    <b>TRUE</b> indicates it should be deleted; <b>FALSE</b> indicates it should be added.

### -param wszId [in]

ID of the revocation authority posting the revocation list. This must match the ID given in the <b>ISSUER</b> node of the revocation list.

### -param wszIdType [in]

Type of ID used by <i>wszId</i>.

### -param wszURL [in]

URL of revocation file list.

### -param pstFrequency [in]

How often the list must be updated.

### -param wszName [in]

Optional human-readable name for a revocation list site.

### -param wszPublicKey [in]

Public key of key pair used to sign and verify the revocation list.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

A revocation list can revoke end-user licenses, server licensor certificates, or almost anything else with an identifying GUID. For a list of the items that can be revoked, see <a href="/previous-versions/windows/desktop/adrms_sdk/revocation">Revocation</a>. The URL provided should refer to the list file itself. The rights management system handles checking for a valid revocation list. This function should only be called once, since subsequent calls will overwrite the previous revocation point in the issuance license.

The public key must be a base-64 encoded string.

Note that if there is no revocation point set in the license, the license can still be revoked by a revocation list signed by the issuer of the license.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetrevocationpoint">DRMGetRevocationPoint</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/revoking-a-certificate">Revoking a Certificate</a>