---
UID: NF:certenroll.IX509CertificateRequestPkcs10.InitializeDecode
title: IX509CertificateRequestPkcs10::InitializeDecode
author: windows-sdk-content
description: Decodes an existing signed or unsigned PKCS #10 certificate request and uses it to initialize the new PKCS #10 request object.
old-location: security\ix509certificaterequestpkcs10_initializedecode_method.htm
tech.root: seccertenroll
ms.assetid: 10ab62c3-9c6f-4e1b-8a86-131d08282d9c
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],InitializeDecode method, IX509CertificateRequestPkcs10.InitializeDecode, IX509CertificateRequestPkcs10::InitializeDecode, InitializeDecode, InitializeDecode method [Security], InitializeDecode method [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::InitializeDecode, security.ix509certificaterequestpkcs10_initializedecode_method
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
 - IX509CertificateRequestPkcs10.InitializeDecode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestPkcs10::InitializeDecode


## -description


The <b>InitializeDecode</b> method decodes an existing signed or unsigned PKCS #10 certificate request and uses it to initialize the new PKCS #10 request object.  The existing request is contained in a byte array that has been encoded by using  <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) as defined by the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) standard. The byte array is represented by a string that is either a pure binary sequence or is Unicode encoded.


## -parameters




### -param strEncodedData [in]

A <b>BSTR</b> variable that contains the DER-encoded  request. For more information, see Remarks.


### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the input string that contains the DER-encoded request. The default value is <b>XCN_CRYPT_STRING_BASE64</b>.


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
The certificate request object has already been initialized.

</td>
</tr>
</table>
 




## -remarks



The <b>InitializeDecode</b> method decodes the existing PKCS #10 request and uses the information retrieved to initialize the following collections for the new request object:<ul>
<li>An empty <a href="https://msdn.microsoft.com/beedb57c-1c89-4d16-8514-046e3071fd1e">ICryptAttributes</a> collection.</li>
<li>An empty <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection.</li>
<li>An empty <a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a> collection for attribute and extension OIDs to be suppressed from the new request.</li>
</ul>


The method also:<ul>
<li>Adds the decoded extensions to the <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection.</li>
<li>Adds the decoded attributes to the <a href="https://msdn.microsoft.com/beedb57c-1c89-4d16-8514-046e3071fd1e">ICryptAttributes</a> collection.</li>
<li>Sets the <a href="https://msdn.microsoft.com/7ecde7cb-1a73-4fee-a949-c4bb36e61547">CriticalExtensions</a> property with the decoded critical extensions.</li>
<li>Sets the <a href="https://msdn.microsoft.com/728dba16-cda8-4eca-8cf0-4e6139e3808b">ClientId</a> property.</li>
<li>Sets the <a href="https://msdn.microsoft.com/490a34bc-08b3-4df2-8996-6137bea53420">TemplateObjectId</a> property.</li>
</ul>


By default, the <b>InitializeDecode</b> method assumes that the certificate request to be decoded is for an end user. Beginning with Windows 8 and Windows Server 2012, you can change this default behavior. After creating an instance of the <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> interface, call <b>InitializeDecode</b> by setting the  <i>Encoding</i> parameter to <b>XCN_CRYPT_STRING_BINARY</b> and the <i>strEncodedData</i> parameter to one of the following values:

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




<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>
 

 

