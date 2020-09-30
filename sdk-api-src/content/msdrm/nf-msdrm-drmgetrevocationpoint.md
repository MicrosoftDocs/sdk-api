---
UID: NF:msdrm.DRMGetRevocationPoint
title: DRMGetRevocationPoint function (msdrm.h)
description: Retrieves information about the revocation point for an issuance license.
helpviewer_keywords: ["DRMGetRevocationPoint","DRMGetRevocationPoint function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetRevocationPoint","rm.drmgetrevocationpoint"]
old-location: rm\drmgetrevocationpoint.htm
tech.root: rm
ms.assetid: 11197e77-0b7f-4972-83a1-a82aa5cef0dd
ms.date: 12/05/2018
ms.keywords: DRMGetRevocationPoint, DRMGetRevocationPoint function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetRevocationPoint, rm.drmgetrevocationpoint
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
 - DRMGetRevocationPoint
 - msdrm/DRMGetRevocationPoint
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
 - DRMGetRevocationPoint
---

# DRMGetRevocationPoint function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetRevocationPoint</b> function retrieves information about the revocation point for an issuance license.

## -parameters

### -param hIssuanceLicense [in]

A handle to the issuance license to get the information from.

### -param puIdLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszId</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszId</i> buffer.

### -param wszId [out]

A pointer to a null-terminated Unicode string that receives the GUID that identifies the revocation point. The size of this buffer is specified by the <i>puIdLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puIdLength</i> value.

### -param puIdTypeLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszIdType</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszIdType</i> buffer.

### -param wszIdType [out]

A pointer to a null-terminated Unicode string that receives the type of the revocation point identifier. The size of this buffer is specified by the <i>puIdTypeLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puIdTypeLength</i> value.

### -param puURLLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszURL</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszURL</i> buffer.

### -param wszRL [out]

A pointer to a null-terminated Unicode string that receives the URL where a revocation list can be obtained. The size of this buffer is specified by the <i>puURLLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puURLLength</i> value.

### -param pstFrequency [out]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that receives the frequency that the revocation list must be refreshed. This parameter is required and cannot be <b>NULL</b>.

### -param puNameLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszName</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszName</i> buffer.

### -param wszName [out]

A pointer to a null-terminated Unicode string that receives the human-readable name for the revocation location. The size of this buffer is specified by the <i>puNameLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puNameLength</i> value.

### -param puPublicKeyLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszPublicKey</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszPublicKey</i> buffer.

### -param wszPublicKey [out]

A pointer to a null-terminated Unicode string that receives the optional public key to identify a revocation list outside the content's chain of trust. The size of this buffer is specified by the <i>puPublicKeyLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puPublicKeyLength</i> value.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

A revocation list can revoke end-user licenses, server licensor certificates, or almost anything else that has an identifying GUID. The URL provided should refer to the list file itself. Active Directory Rights Management Services (AD RMS) handles checking for a valid revocation list. You could call this function for each revocation point structure in a license if <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateboundlicense">DRMCreateBoundLicense</a> fails because of a stale or missing revocation list. However, a simpler method is to call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmacquireadvisories">DRMAcquireAdvisories</a>, which updates all revocation lists for you.

If a public key is provided, it should be a well-formed XrML public key node. If the revocation list is signed with a key pair outside the content's chain of trust, the public key of that key pair must be specified here. Otherwise, it should not be used.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetrevocationpoint">DRMSetRevocationPoint</a>