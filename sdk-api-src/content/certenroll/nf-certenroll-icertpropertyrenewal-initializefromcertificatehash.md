---
UID: NF:certenroll.ICertPropertyRenewal.InitializeFromCertificateHash
title: ICertPropertyRenewal::InitializeFromCertificateHash
author: windows-sdk-content
description: Initializes the object from the new certificate.
old-location: security\icertpropertyrenewal_initializefromcertificatehash_method.htm
tech.root: SecCertEnroll
ms.assetid: 87e0eabf-7a4a-4ff2-a9ce-6482f119cafd
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICertPropertyRenewal interface [Security],InitializeFromCertificateHash method, ICertPropertyRenewal.InitializeFromCertificateHash, ICertPropertyRenewal::InitializeFromCertificateHash, InitializeFromCertificateHash, InitializeFromCertificateHash method [Security], InitializeFromCertificateHash method [Security],ICertPropertyRenewal interface, certenroll/ICertPropertyRenewal::InitializeFromCertificateHash, security.icertpropertyrenewal_initializefromcertificatehash_method
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
 - ICertPropertyRenewal.InitializeFromCertificateHash
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertPropertyRenewal::InitializeFromCertificateHash


## -description


The <b>InitializeFromCertificateHash</b> method initializes the object from the new  certificate.


## -parameters




### -param MachineContext [in]

A <b>VARIANT_BOOL</b> value that indicates  whether the certificate store is for the local computer or the current user. Specify <b>VARIANT_TRUE</b> for the computer and <b>VARIANT_FALSE</b> for the user.


### -param Encoding [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa374936(v=VS.85).aspx">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the input string that contains the DER-encoded certificate.


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

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

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
The object is already initialized.

</td>
</tr>
</table>
 




## -remarks



 This method creates a SHA-1 hash by using the specified certificate. The certificate must be encoded by using <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) as defined by the <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) standard. You must also specify the type of Unicode encoding applied to the string that contains the DER-encoded certificate.

Typically the <a href="https://msdn.microsoft.com/en-us/library/Aa375749(v=VS.85).aspx">ICertPropertyRenewal</a> object is initialized during the enrollment process. You can retrieve the certificate used during enrollment by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa377867(v=VS.85).aspx">Certificate</a> property on the <a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a> interface.

Call the <a href="https://msdn.microsoft.com/en-us/library/Aa375928(v=VS.85).aspx">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="https://msdn.microsoft.com/en-us/library/Aa375766(v=VS.85).aspx">Renewal</a> property to retrieve the hash.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375749(v=VS.85).aspx">ICertPropertyRenewal</a>
 

 

