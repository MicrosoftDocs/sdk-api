---
UID: NF:certenroll.IX509Enrollment.CreatePFX
title: IX509Enrollment::CreatePFX (certenroll.h)
description: Creates a Personal Information Exchange (PFX) message.
helpviewer_keywords: ["CreatePFX","CreatePFX method [Security]","CreatePFX method [Security]","IX509Enrollment interface","IX509Enrollment interface [Security]","CreatePFX method","IX509Enrollment.CreatePFX","IX509Enrollment::CreatePFX","certenroll/IX509Enrollment::CreatePFX","security.ix509enrollment_createpfx_method"]
old-location: security\ix509enrollment_createpfx_method.htm
tech.root: security
ms.assetid: 4a51bea0-e7f8-4a4e-b612-95616b126466
ms.date: 12/05/2018
ms.keywords: CreatePFX, CreatePFX method [Security], CreatePFX method [Security],IX509Enrollment interface, IX509Enrollment interface [Security],CreatePFX method, IX509Enrollment.CreatePFX, IX509Enrollment::CreatePFX, certenroll/IX509Enrollment::CreatePFX, security.ix509enrollment_createpfx_method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509Enrollment::CreatePFX
 - certenroll/IX509Enrollment::CreatePFX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509Enrollment.CreatePFX
---

# IX509Enrollment::CreatePFX


## -description

The <b>CreatePFX</b> method creates a Personal Information Exchange (PFX) message. The message is contained in a byte array that is encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) as defined by the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) standard.  The DER-encoded byte array is represented by a string that is either a pure binary sequence or is Unicode encoded.

## -parameters

### -param strPassword [in]

A <b>BSTR</b> variable that contains a password for the PFX message. This can be  <b>NULL</b> to indicate that  no password is used.  When you have finished using the password, clear it from memory by calling the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function. For more information about protecting the password, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

### -param ExportOptions [in]

A <a href="/windows/desktop/api/certenroll/ne-certenroll-pfxexportoptions">PFXExportOptions</a> enumeration value that specifies how much of the certificate chain is exported. You can export the certificate only, the certificate chain without the root, or the entire chain.

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the DER-encoded  message. The default value is <b>XCN_CRYPT_STRING_BASE64</b>.

### -param pValue [out]

Pointer to a <b>BSTR</b> variable that contains the DER-encoded PFX message.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The certificate cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
No  certificate chain can be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The enrollment object has not been initialized.

</td>
</tr>
</table>

## -remarks

The PFX format is also known as PKCS #12. The <b>CreatePFX</b> method:<ul>
<li>Opens the certificate store in memory for the default provider.</li>
<li>Adds the installed certificate to the store or builds the certificate chain adds a link to it.</li>
<li>Exports the certificate and the private key to a PFX message depending on the export options specified.</li>
<li>Encodes the exported message by using DER.</li>
</ul>


Before calling this method, you must initialize the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a> object by calling one of the following methods.<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-initialize">Initialize</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-initializefromrequest">InitializeFromRequest</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-initializefromtemplatename">InitializeFromTemplateName</a>
</li>
</ul>Further, you must return successfully from the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-enroll">Enroll</a> method.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a>