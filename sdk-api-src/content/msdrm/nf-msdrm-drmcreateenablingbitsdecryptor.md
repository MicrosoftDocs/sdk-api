---
UID: NF:msdrm.DRMCreateEnablingBitsDecryptor
title: DRMCreateEnablingBitsDecryptor function (msdrm.h)
description: Creates a decryption object that is used to decrypt content data.
helpviewer_keywords: ["DRMCreateEnablingBitsDecryptor","DRMCreateEnablingBitsDecryptor function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMCreateEnablingBitsDecryptor","rm.drmcreateenablingbitsdecryptor"]
old-location: rm\drmcreateenablingbitsdecryptor.htm
tech.root: rm
ms.assetid: 133582e2-6396-476f-a28b-37ed0257fb79
ms.date: 12/05/2018
ms.keywords: DRMCreateEnablingBitsDecryptor, DRMCreateEnablingBitsDecryptor function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCreateEnablingBitsDecryptor, rm.drmcreateenablingbitsdecryptor
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
 - DRMCreateEnablingBitsDecryptor
 - msdrm/DRMCreateEnablingBitsDecryptor
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
 - DRMCreateEnablingBitsDecryptor
---

# DRMCreateEnablingBitsDecryptor function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCreateEnablingBitsDecryptor</b> function creates a decryption object that is used to decrypt content data.

## -parameters

### -param hBoundLicense [in]

A handle to a bound license object created by using <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateboundlicense">DRMCreateBoundLicense</a>.

### -param wszRight [in, optional]

An optional null-terminated string that contains the right to exercise. A decrypting object can be bound to only one right at a time.

### -param hAuxLib [in]

Reserved for future use. This parameter must be <b>NULL</b>.

### -param wszAuxPlug [in, optional]

Reserved for future use. This parameter must be <b>NULL</b>.

### -param phDecryptor [out]

A pointer to the decrypting object.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

A consuming application performs the following steps to decrypt content previously encrypted by a publishing application.<ol>
<li>Retrieve an end-user license. Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmenumeratelicense">DRMEnumerateLicense</a> to retrieve the license if it already exists in the store. If function succeeds, go to step 2. If the license is not in the store, call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmacquirelicense">DRMAcquireLicense</a> followed by <b>DRMEnumerateLicense</b>.</li>
<li>Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateboundlicense">DRMCreateBoundLicense</a> to create a license that binds to one or more rights in the end-user license. The bound license includes a symmetric key that can be used for decryption.</li>
<li>Call <b>DRMCreateEnablingBitsDecryptor</b> to create a decrypting object associated with the bound right and content key.</li>
<li>Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmdecrypt">DRMDecrypt</a> to use the content key to decrypt the content.</li>
</ol>


Call the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosehandle">DRMCloseHandle</a> function to close the decrypting object handle when you are finished with it. Both the decrypting object handle and the bound license handle must remain open until decryption is complete.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateenablingbitsencryptor">DRMCreateEnablingBitsEncryptor</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/decrypting-content">Decrypting Content</a>