---
UID: NF:certenroll.IX509CertificateRequestPkcs7.InitializeDecode
title: IX509CertificateRequestPkcs7::InitializeDecode method
author: windows-driver-content
description: Decodes an existing signed or unsigned PKCS #7 request object and uses it to initialize the new PKCS #7 object.
old-location: security\ix509certificaterequestpkcs7_initializedecode_method.htm
old-project: SecCertEnroll
ms.assetid: 40084cb0-eb48-485d-aa45-8ddb577f2d4f
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IX509CertificateRequestPkcs7, IX509CertificateRequestPkcs7 interface [Security], InitializeDecode method, IX509CertificateRequestPkcs7::InitializeDecode, InitializeDecode method [Security], InitializeDecode method [Security], IX509CertificateRequestPkcs7 interface, InitializeDecode,IX509CertificateRequestPkcs7.InitializeDecode, certenroll/IX509CertificateRequestPkcs7::InitializeDecode, security.ix509certificaterequestpkcs7_initializedecode_method
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509CertificateRequestPkcs7.InitializeDecode
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestPkcs7::InitializeDecode method


## -description


The <b>InitializeDecode</b> method decodes an existing signed or unsigned PKCS #7 request object and uses it to initialize the new PKCS #7  object. The existing request is contained in a byte array that has been encoded by using  <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) as defined by the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) standard. The byte array is represented by a string that is either a pure binary sequence or is Unicode encoded.


## -parameters




### -param strEncodedData [in]

A <b>BSTR</b> variable that contains the DER-encoded  request.


### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the input string that contains the DER-encoded  request. The default value is <b>XCN_CRYPT_STRING_BASE64</b>.


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
The request object has already been initialized.

</td>
</tr>
</table>
 




## -remarks



The <b>InitializeDecode</b> method:<ul>
<li>Decodes the PKCS #7 request specified on input.</li>
<li>Uses the decoded object to create an inner PKCS #10 request with the following collections:<ul>
<li>An empty <a href="https://msdn.microsoft.com/beedb57c-1c89-4d16-8514-046e3071fd1e">ICryptAttributes</a> collection.</li>
<li>An empty <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection.</li>
<li>An empty <a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a> collection for critical extensions.</li>
<li>An empty <a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a> collection for attribute and extension OIDs to be suppressed from the new request.</li>
</ul>
</li>
<li>Adds the decoded extensions to the <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection.</li>
<li>Adds the decoded attributes to the <a href="https://msdn.microsoft.com/beedb57c-1c89-4d16-8514-046e3071fd1e">ICryptAttributes</a> collection</li>
<li>Sets the <a href="https://msdn.microsoft.com/728dba16-cda8-4eca-8cf0-4e6139e3808b">ClientId</a> property.</li>
<li>Sets the <a href="https://msdn.microsoft.com/490a34bc-08b3-4df2-8996-6137bea53420">TemplateObjectId</a> property.</li>
<li>Uses the signature on the original PKCS #7 request to create a new <a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a> object.</li>
<li>Retrieves an <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object from the <a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a> object.</li>
<li>Initializes the new <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object by using the original signature and hash algorithms.</li>
<li>Sets the PKCS #10 request as the inner request object.</li>
</ul>


By default, the <b>InitializeDecode</b> method assumes that the certificate request to be decoded is for an end user. Beginning with Windows 8 and Windows Server 2012, you can change this default behavior. After creating an instance of the <a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a> interface, call <b>InitializeDecode</b> by setting the  <i>Encoding</i> parameter to <b>XCN_CRYPT_STRING_BINARY</b> and the <i>strEncodedData</i> parameter to one of the following values:

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>L"ContextMachine"</td>
<td>The encoded certificate request is for a computer.

</td>
</tr>
<tr>
<td>L"ContextUser"</td>
<td>The encoded certificate request is for an end user.</td>
</tr>
<tr>
<td>L"ContextAdministratorForceMachine"</td>
<td>The encoded certificate is being requested by an administrator acting on the behalf of a computer.

</td>
</tr>
</table>
 

Then, call the <b>InitializeDecode</b> method again with the encoded certificate set in the <i>strEncodedData</i> argument.




## -see-also




<a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>
 

 

