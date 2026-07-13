---
UID: NF:msi.MsiGetFileSignatureInformationW
title: MsiGetFileSignatureInformationW function (msi.h)
description: The MsiGetFileSignatureInformation function takes the path to a file that has been digitally signed and returns the file's signer certificate and hash. (Unicode)
helpviewer_keywords: ["MSI_INVALID_HASH_IS_FATAL", "MsiGetFileSignatureInformation", "MsiGetFileSignatureInformation function", "MsiGetFileSignatureInformationW", "_msi_msigetfilesignatureinformation", "msi/MsiGetFileSignatureInformation", "msi/MsiGetFileSignatureInformationW", "setup.msigetfilesignatureinformation"]
old-location: setup\msigetfilesignatureinformation.htm
tech.root: setup
ms.assetid: a3f8b8ef-2d2e-4375-a2bb-08a53a94fb16
ms.date: 12/05/2018
ms.keywords: MSI_INVALID_HASH_IS_FATAL, MsiGetFileSignatureInformation, MsiGetFileSignatureInformation function, MsiGetFileSignatureInformationA, MsiGetFileSignatureInformationW, _msi_msigetfilesignatureinformation, msi/MsiGetFileSignatureInformation, msi/MsiGetFileSignatureInformationA, msi/MsiGetFileSignatureInformationW, setup.msigetfilesignatureinformation
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetFileSignatureInformationW (Unicode) and MsiGetFileSignatureInformationA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiGetFileSignatureInformationW
 - msi/MsiGetFileSignatureInformationW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiGetFileSignatureInformation
 - MsiGetFileSignatureInformationA
 - MsiGetFileSignatureInformationW
---

# MsiGetFileSignatureInformationW function


## -description

The 
<b>MsiGetFileSignatureInformation</b> function takes the path to a file that has been digitally signed and returns the file's signer certificate and hash. 
<b>MsiGetFileSignatureInformation</b> may be called to obtain the signer certificate and hash needed to populate the 
<a href="/windows/desktop/Msi/msidigitalcertificate-table">MsiDigitalCertificate</a>, <a href="/windows/desktop/Msi/msipatchcertificate-table">MsiPatchCertificate</a>, and 
<a href="/windows/desktop/Msi/msidigitalsignature-table">MsiDigitalSignature</a> tables.




<b>Windows Installer 3.0 and later:  </b>Beginning with Windows Installer 3.0, the Windows Installer can verify the digital signatures of patches (.msp files) by using the <a href="/windows/desktop/Msi/msipatchcertificate-table">MsiPatchCertificate</a> and <a href="/windows/desktop/Msi/msidigitalcertificate-table">MsiDigitalCertificate</a> tables. For more information see <a href="/windows/desktop/Msi/guidelines-for-authoring-secure-installations">Guidelines for Authoring Secure Installations</a> and <a href="/windows/desktop/Msi/user-account-control--uac--patching">User Account Control (UAC) Patching</a>. 

 


<b>Windows Installer 2.0:  </b>Digital signatures of patches is not supported. Windows Installer 2.0 uses digital signatures as a means to detect corrupted resources, and can only verify the digital signatures of external cabinets, and only by the use of the <a href="/windows/desktop/Msi/msidigitalsignature-table">MsiDigitalSignature</a> and <a href="/windows/desktop/Msi/msidigitalcertificate-table">MsiDigitalCertificate</a> tables.

## -parameters

### -param szSignedObjectPath [in]

Pointer to a null-terminated string specifying the full path to the file that contains the digital signature.

### -param dwFlags [in]

Special error case flags. 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSI_INVALID_HASH_IS_FATAL"></a><a id="msi_invalid_hash_is_fatal"></a><dl>
<dt><b>MSI_INVALID_HASH_IS_FATAL</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Without this flag set, and when requesting only the certificate context, an invalid hash in the digital signature does not cause 
<b>MsiGetFileSignatureInformation</b> to return a fatal error. 




To return a fatal error for an invalid hash, set the MSI_INVALID_HASH_IS_FATAL flag.

</td>
</tr>
</table>

### -param ppcCertContext [out]

Returned signer certificate context

### -param pbHashData [out]

Returned hash buffer. This parameter can be <b>NULL</b> if the hash data is not being requested.

### -param pcbHashData [in, out]

Pointer to a variable that specifies the size, in bytes, of the buffer pointed to by the <i>pbHashData</i> parameter. This parameter cannot be <b>NULL</b> if <i>pbHashData</i> is non-<b>NULL</b>. If ERROR_MORE_DATA is returned, <i>pbHashData</i> gives the size of the buffer required to hold the hash data. If ERROR_SUCCESS is returned, it gives the number of bytes written to the hash buffer. The <i>pcbHashData</i> parameter is ignored if <i>pbHashData</i> is <b>NULL</b>.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS/S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successful completion.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Invalid parameter was specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a> is not available on the system. 
<b>MsiGetFileSignatureInformation</b> requires the presence of the Wintrust.dll file on the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
A buffer is too small to hold the requested data. If ERROR_MORE_DATA is returned, <i>pcbHashData</i> gives the size of the buffer required to hold the hash data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUST_E_NOSIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
File is not signed

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUST_E_BAD_DIGEST</b></dt>
</dl>
</td>
<td width="60%">
The file's current hash is invalid according to the hash stored in the file's digital signature.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERT_E_REVOKED</b></dt>
</dl>
</td>
<td width="60%">
The file's signer certificate has been revoked. The file's digital signature is compromised.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUST_E_SUBJECT_NOT_TRUSTED</b></dt>
</dl>
</td>
<td width="60%">
The subject failed the specified verification action. Most trust providers return a more detailed error code that describes the reason for the failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUST_E_PROVIDER_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The trust provider is not recognized on this system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUST_E_ACTION_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The trust provider does not support the specified action.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUST_E_SUBJECT_FORM_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The trust provider does not support the form specified for the subject.

</td>
</tr>
</table>
 


<div> </div>


<b>MsiGetFileSignatureInformation</b> also returns all the Win32 error values mapped to their equivalent <b>HRESULT</b> data type by 
<b>HRESULT_FROM_WIN32</b>.

## -remarks

When requesting only the certificate context, an invalid hash in the digital signature does not cause 
<b>MsiGetFileSignatureInformation</b> to return a fatal error. To return a fatal error for an invalid hash, set the MSI_INVALID_HASH_IS_FATAL flag in the <i>dwFlags</i> parameter.

The certificate context and hash information is extracted from the file by a call to <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a>. The <i>ppcCertContext</i> parameter is a duplicate of the signer certificate context from the signature. It is the responsibility of the caller to call <i>CertFreeCertificateContext</i> to free the certificate context when finished.

Note that 
<b>MsiGetFileSignatureInformation</b> requires the presence of the Wintrust.dll file on the system.





> [!NOTE]
> The msi.h header defines MsiGetFileSignatureInformation as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/digital-signatures-and-windows-installer">Digital Signatures and Windows Installer</a>



<a href="/windows/desktop/Msi/msidigitalcertificate-table">MsiDigitalCertificate table</a>



<a href="/windows/desktop/Msi/msidigitalsignature-table">MsiDigitalSignature table</a>
