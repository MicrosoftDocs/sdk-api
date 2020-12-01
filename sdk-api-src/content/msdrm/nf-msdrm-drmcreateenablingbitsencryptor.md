---
UID: NF:msdrm.DRMCreateEnablingBitsEncryptor
title: DRMCreateEnablingBitsEncryptor function (msdrm.h)
description: Creates an AD RMS encrypting object that is used to encrypt content data.
helpviewer_keywords: ["DRMCreateEnablingBitsEncryptor","DRMCreateEnablingBitsEncryptor function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMCreateEnablingBitsEncryptor","rm.drmcreateenablingbitsencryptor"]
old-location: rm\drmcreateenablingbitsencryptor.htm
tech.root: rm
ms.assetid: f3875ddd-293e-4abb-b468-a6754bc361a0
ms.date: 12/05/2018
ms.keywords: DRMCreateEnablingBitsEncryptor, DRMCreateEnablingBitsEncryptor function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCreateEnablingBitsEncryptor, rm.drmcreateenablingbitsencryptor
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
 - DRMCreateEnablingBitsEncryptor
 - msdrm/DRMCreateEnablingBitsEncryptor
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
 - DRMCreateEnablingBitsEncryptor
---

# DRMCreateEnablingBitsEncryptor function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCreateEnablingBitsEncryptor</b> function creates an AD RMS encrypting object that is used to encrypt content data.

## -parameters

### -param hBoundLicense [in]

A handle to a bound license, produced by <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateboundlicense">DRMCreateBoundLicense</a>.

### -param wszRight [in, optional]

Optional null-terminated string containing a right. If you specify <b>NULL</b>, the AD RMS encrypting object binds to the first valid right in the license.

### -param hAuxLib [in]

Reserved for future use. This parameter must be <b>NULL</b>.

### -param wszAuxPlug [in, optional]

Reserved for future use. This parameter must be <b>NULL</b>.

### -param phEncryptor [out]

A pointer to the encrypting object.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Perform the following steps to encrypt content. For more information, see <a href="/previous-versions/windows/desktop/adrms_sdk/encrypting-content">Encrypting Content</a>.<ul>
<li>Acquire an end-user license. If the issuance license that you are using for this purpose was signed online, call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmacquirelicense">DRMAcquireLicense</a> followed by  <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmenumeratelicense">DRMEnumerateLicense</a>. If the issuance license was signed offline, call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetownerlicense">DRMGetOwnerLicense</a> instead.</li>
<li>Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateboundlicense">DRMCreateBoundLicense</a> to create a license that binds to the EDIT or OWNER right in the end-user license. The bound license includes a symmetric key that can be used for encryption.</li>
<li>Call <b>DRMCreateEnablingBitsEncryptor</b> to create an encrypting object associated with the bound right and content key.</li>
<li>Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmencrypt">DRMEncrypt</a> to use the content key to encrypt the content.</li>
</ul>


Call the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosehandle">DRMCloseHandle</a> function to close the encrypting object handle when you are finished with it. Both the encrypting object handle and the bound license handle must remain open until encryption is complete.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/creating-and-using-issuance-licenses">Creating and Using Issuance Licenses</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateenablingbitsdecryptor">DRMCreateEnablingBitsDecryptor</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/encrypting-content">Encrypting Content</a>