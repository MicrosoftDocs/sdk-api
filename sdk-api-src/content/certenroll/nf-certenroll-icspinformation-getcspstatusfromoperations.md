---
UID: NF:certenroll.ICspInformation.GetCspStatusFromOperations
title: ICspInformation::GetCspStatusFromOperations
author: windows-driver-content
description: Creates an ICspStatus object for the first supported algorithm that is consistent with the specified signature, encryption, hashing, or cipher operation.
old-location: security\icspinformation_getcspstatusfromoperations.htm
old-project: SecCertEnroll
ms.assetid: 6b551e72-2f0a-4ae8-ba06-dff1508a7d83
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: GetCspStatusFromOperations, GetCspStatusFromOperations method [Security], GetCspStatusFromOperations method [Security],ICspInformation interface, ICspInformation interface [Security],GetCspStatusFromOperations method, ICspInformation.GetCspStatusFromOperations, ICspInformation::GetCspStatusFromOperations, certenroll/ICspInformation::GetCspStatusFromOperations, security.icspinformation_getcspstatusfromoperations
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
-	ICspInformation.GetCspStatusFromOperations
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICspInformation::GetCspStatusFromOperations


## -description


The <b>GetCspStatusFromOperations</b> method  creates an <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> object for the first supported algorithm that is consistent with the specified signature, encryption, hashing, or cipher  operation.


## -parameters




### -param pAlgorithm [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> interface that represents an algorithm OID. This parameter is optional and can be <b>NULL</b>.   

<ul>
<li>If you specify an OID and set the <i>Operations</i>  parameter to <b>XCN_NCRYPT_SIGNATURE_OPERATION</b> and combine this flag with either XCN_NCRYPT_EXACT_MATCH_OPERATION or XCN_NCRYPT_PREFER_SIGNATURE_ONLY_OPERATION, the first signature algorithm, if any, that matches the OID is used.</li>
<li>If you specify an OID but do not set the  <i>Operations</i>  parameter to <b>XCN_NCRYPT_SIGNATURE_OPERATION</b>, or you set <b>XCN_NCRYPT_SIGNATURE_OPERATION</b> but do not combine it with either XCN_NCRYPT_EXACT_MATCH_OPERATION or XCN_NCRYPT_PREFER_SIGNATURE_ONLY_OPERATION, the first algorithm that can be used for signing or encryption is used.</li>
<li>If you do not specify an OID, the first supported algorithm consistent with the flags specified in the  <i>Operations</i> parameter is used.</li>
</ul>

### -param Operations [in]

An <a href="https://msdn.microsoft.com/5fa7ee1e-f5ab-44c9-8ae4-a2940f0c6289">AlgorithmOperationFlags</a>  enumeration value that identifies the type of algorithm to retrieve. One of the following values must be specified:<ul>
<li>XCN_NCRYPT_CIPHER_OPERATION</li>
<li>XCN_NCRYPT_HASH_OPERATION</li>
<li>XCN_NCRYPT_SIGNATURE_OPERATION</li>
<li>XCN_NCRYPT_SECRET_AGREEMENT_OPERATION</li>
<li>XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION</li>
</ul>


You can refine the search characteristics by combining one of the preceding flags with one of the following:<ul>
<li>XCN_NCRYPT_PREFER_SIGNATURE_ONLY_OPERATION</li>
<li>XCN_NCRYPT_PREFER_NON_SIGNATURE_OPERATION</li>
<li>XCN_NCRYPT_EXACT_MATCH_OPERATION</li>
</ul>


If you set the XCN_NCRYPT_PREFER_SIGNATURE_ONLY_OPERATION or XCN_NCRYPT_PREFER_NON_SIGNATURE_OPERATION preference flags, you cannot also specify either of the following:


<ul>
<li>XCN_NCRYPT_CIPHER_OPERATION</li>
<li>XCN_NCRYPT_HASH_OPERATION</li>
</ul>



### -param ppValue [out]

Address of a variable that receives a pointer to an  <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> interface.


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
The <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> object could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>OLE_E_BLANK</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> object has not been initialized.

</td>
</tr>
</table>
 




## -remarks



An <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> object contains status information about a cryptographic provider. Each object is initialized for a specific algorithm supported by the provider. If you do not specify an algorithm in the <i>pAlgorithm</i> parameter, the first supported algorithm that is consistent with the permitted operations is chosen to create the <b>ICspStatus</b> object.




## -see-also




<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>
 

 

