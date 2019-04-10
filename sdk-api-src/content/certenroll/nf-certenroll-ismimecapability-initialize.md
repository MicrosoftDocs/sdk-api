---
UID: NF:certenroll.ISmimeCapability.Initialize
title: ISmimeCapability::Initialize (certenroll.h)
author: windows-sdk-content
description: Initializes the object from a symmetric encryption algorithm object identifier (OID) and an optional key length.
old-location: security\ismimecapability_initialize_method.htm
tech.root: seccertenroll
ms.assetid: d972121d-ecfa-4a79-9322-dd0d0b81ba68
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISmimeCapability interface [Security],Initialize method, ISmimeCapability.Initialize, ISmimeCapability::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ISmimeCapability interface, certenroll/ISmimeCapability::Initialize, security.ismimecapability_initialize_method
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
 - ISmimeCapability.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISmimeCapability::Initialize


## -description


The <b>Initialize</b> method initializes the object from a symmetric encryption algorithm <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and an optional key length.


## -parameters




### -param pObjectId [in]

Pointer to an <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> interface that represents the OID.


### -param BitCount [in]

A <b>LONG</b> variable that contains the bit length of the symmetric key.


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
<dt><b><b>CERTSRV_E_PROPERTY_EMPTY</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> pointer is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The following symmetric encryption algorithms are supported by the Certificate Enrollment API. Only the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">RC2</a> and <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">RC4</a> algorithms have variable key lengths that can be specified.<table>
<tr>
<th>OID</th>
<th>Key length</th>
<th>Description</th>
</tr>
<tr>
<td>XCN_OID_OIWSEC_desCBC1.3.14.3.2.7

</td>
<td>56</td>
<td>The key size is of the DES CBC algorithm is 56 bits. You do not need to specify this value.</td>
</tr>
<tr>
<td>XCN_OID_RSA_DES_EDE3_CBC1.2.840.113549.3.7

</td>
<td>168</td>
<td>The key size is of the 3DES CBC algorithm is 168 bits. You do not need to specify this value.</td>
</tr>
<tr>
<td>XCN_OID_RSA_RC2CBC1.2.840.113549.3.2

</td>
<td>40 to 128</td>
<td>RC4 is a variable key algorithm. common values are 40, 64, and 128 bits.</td>
</tr>
<tr>
<td>XCN_OID_RSA_RC41.2.840.113549.3.4

</td>
<td>40 to 128</td>
<td>RC4 is a variable key algorithm. common values are 40, 64, and 128 bits.</td>
</tr>
<tr>
<td>XCN_OID_RSA_SMIMEalgCMS3DESwrap1.2.840.113549.1.9.16.3.6

</td>
<td>168</td>
<td>The key size of the MMS <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Data Encryption Standard</a> (DES) key wrap algorithm is 168 bits. You do not need to specify this value. </td>
</tr>
<tr>
<td>XCN_OID_RSA_SMIMEalgCMSRC2wrap1.2.840.113549.1.9.16.3.7

</td>
<td>128</td>
<td>The key size of the MMS RC2 key wrap algorithm is 128 bits. You do not need to specify this value.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES128_CBC2.16.840.1.101.3.4.1.2

</td>
<td>128</td>
<td>The key size is implied by the OID. You do not need to specify this value.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES192_CBC2.16.840.1.101.3.4.1.22

</td>
<td>192</td>
<td>The key size is implied by the OID. You do not need to specify this value.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES256_CBC2.16.840.1.101.3.4.1.42

</td>
<td>256</td>
<td>The key size is implied by the OID. You do not need to specify this value.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES128_WRAP2.16.840.1.101.3.4.1.5

</td>
<td>128</td>
<td>The key size is implied by the OID. You do not need to specify this value.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES192_WRAP2.16.840.1.101.3.4.1.25

</td>
<td>192</td>
<td>The key size is implied by the OID. You do not need to specify this value.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES256_WRAP2.16.840.1.101.3.4.1.45

</td>
<td>256</td>
<td>The key size is implied by the OID. You do not need to specify this value.</td>
</tr>
</table>
 



The key length that you specify for RC2 and RC4 algorithms must be consistent with that supported by the cryptographic provider or providers used by the client. For more information, see <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>. You can retrieve the bit length by calling the <a href="https://msdn.microsoft.com/582f5d85-9045-4c6f-a4c0-869e6f9e9b9e">BitCount</a> property,  and you can retrieve the algorithm OID by calling the <a href="https://msdn.microsoft.com/3bd773f2-f3ea-45e5-9b37-8346070049d8">ObjectId</a> property.




## -see-also




<a href="https://msdn.microsoft.com/f9750b68-9d35-4594-96fc-2fbd54a87dcc">ISmimeCapabilities</a>



<a href="https://msdn.microsoft.com/3cfbb16f-88fa-41f1-b719-cd5e8ad636cc">ISmimeCapability</a>



<a href="https://msdn.microsoft.com/06dca62d-282b-4bdd-bc8d-4d2e6eb226b5">IX509ExtensionSmimeCapabilities</a>
 

 

