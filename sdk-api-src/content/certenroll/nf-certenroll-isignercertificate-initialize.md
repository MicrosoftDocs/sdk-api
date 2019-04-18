---
UID: NF:certenroll.ISignerCertificate.Initialize
title: ISignerCertificate::Initialize (certenroll.h)
author: windows-sdk-content
description: Initializes the object from a signing certificate.
old-location: security\isignercertificate_initialize_method.htm
tech.root: seccertenroll
ms.assetid: 2553f0bc-a177-49fc-932f-080cb4bd7a5c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISignerCertificate interface [Security],Initialize method, ISignerCertificate.Initialize, ISignerCertificate::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ISignerCertificate interface, certenroll/ISignerCertificate::Initialize, security.isignercertificate_initialize_method
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ISignerCertificate.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISignerCertificate::Initialize


## -description


The <b>Initialize</b> method initializes the object from a signing certificate.


## -parameters




### -param MachineContext [in]

A <b>VARIANT_BOOL</b> variable that indicates whether to search the local computer certificate store context or the user context to find the certificate identified by the <i>strCertificate</i> parameter. Specify <b>VARIANT_TRUE</b> for the computer and <b>VARIANT_FALSE</b> for the user.


### -param VerifyType [in]

An <a href="https://msdn.microsoft.com/23466035-6554-490f-ad46-e97ba5a5d996">X509PrivateKeyVerify</a> enumeration value that specifies whether the private key used to sign the certificate must be verified and, if so, whether the verification must be silent or allows user input.


### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded certificate string.


### -param strCertificate [in]

A <b>BSTR</b> variable that contains the DER-encoded certificate.

Beginning with Windows 7 and Windows Server 2008 R2, you can specify a certificate thumb print or serial number rather than an encoded certificate. Doing so causes the function to search the appropriate local stores for the matching certificate. Keep in mind the following points:

<ul>
<li>The <b>BSTR</b> must be an even number of hexadecimal digits.</li>
<li>Whitespace between hexadecimal pairs is ignored.</li>
<li>The <i>Encoding</i> parameter must be set to <b>XCN_CRYPT_STRING_HEXRAW</b>.</li>
<li>The <i>MachineContext</i> parameter determines whether the user or computer stores or both are searched.</li>
<li>If a private key is needed, only the personal and request stores are searched.</li>
<li>If a private key is not needed, the root and intermediate CA stores are also searched.</li>
</ul>

## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a> object has already been initialized.

</td>
</tr>
</table>
 




## -remarks



The <b>Initialize</b> method:<ul>
<li>Verifies whether the private key associated with the certificate exists.</li>
<li>Creates an <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object and assigns it to the <a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a> object.</li>
<li>Retrieves the public key algorithm from the private key.</li>
<li>Assigns the public key algorithm to the <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object.</li>
</ul>


Set the following properties before calling <b>Initialize</b>:<ul>
<li>
<a href="https://msdn.microsoft.com/a1749c92-11e4-4726-a355-ccdd245b4df8">ParentWindow</a>
</li>
<li>
<a href="https://msdn.microsoft.com/695d895e-0646-4a2e-a699-86674f919bad">Pin</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b598d4a2-d53a-4091-a059-f9674acf9318">Silent</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0fd874b0-9093-4c1b-94a0-a2aaad19010e">UIContextMessage</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a>
 

 

