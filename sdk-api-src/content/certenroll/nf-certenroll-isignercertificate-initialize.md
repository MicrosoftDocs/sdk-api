---
UID: NF:certenroll.ISignerCertificate.Initialize
title: ISignerCertificate::Initialize
author: windows-sdk-content
description: Initializes the object from a signing certificate.
old-location: security\isignercertificate_initialize_method.htm
tech.root: SecCertEnroll
ms.assetid: 2553f0bc-a177-49fc-932f-080cb4bd7a5c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISignerCertificate interface [Security],Initialize method, ISignerCertificate.Initialize, ISignerCertificate::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ISignerCertificate interface, certenroll/ISignerCertificate::Initialize, security.isignercertificate_initialize_method
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# ISignerCertificate::Initialize


## -description


The <b>Initialize</b> method initializes the object from a signing certificate.


## -parameters




### -param MachineContext [in]

A <b>VARIANT_BOOL</b> variable that indicates whether to search the local computer certificate store context or the user context to find the certificate identified by the <i>strCertificate</i> parameter. Specify <b>VARIANT_TRUE</b> for the computer and <b>VARIANT_FALSE</b> for the user.


### -param VerifyType [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa379424(v=VS.85).aspx">X509PrivateKeyVerify</a> enumeration value that specifies whether the private key used to sign the certificate must be verified and, if so, whether the verification must be silent or allows user input.


### -param Encoding [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa374936(v=VS.85).aspx">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded certificate string.


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

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

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
The <a href="https://msdn.microsoft.com/en-us/library/Aa376820(v=VS.85).aspx">ISignerCertificate</a> object has already been initialized.

</td>
</tr>
</table>
 




## -remarks



The <b>Initialize</b> method:<ul>
<li>Verifies whether the private key associated with the certificate exists.</li>
<li>Creates an <a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a> object and assigns it to the <a href="https://msdn.microsoft.com/en-us/library/Aa376820(v=VS.85).aspx">ISignerCertificate</a> object.</li>
<li>Retrieves the public key algorithm from the private key.</li>
<li>Assigns the public key algorithm to the <a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a> object.</li>
</ul>


Set the following properties before calling <b>Initialize</b>:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376834(v=VS.85).aspx">ParentWindow</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376835(v=VS.85).aspx">Pin</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376839(v=VS.85).aspx">Silent</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376840(v=VS.85).aspx">UIContextMessage</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376820(v=VS.85).aspx">ISignerCertificate</a>
 

 

