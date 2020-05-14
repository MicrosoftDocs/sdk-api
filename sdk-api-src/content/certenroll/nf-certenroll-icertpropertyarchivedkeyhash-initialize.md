---
UID: NF:certenroll.ICertPropertyArchivedKeyHash.Initialize
title: ICertPropertyArchivedKeyHash::Initialize (certenroll.h)
description: Initializes the object from a byte array that contains the hash.helpviewer_keywords: ["ICertPropertyArchivedKeyHash interface [Security]","Initialize method","ICertPropertyArchivedKeyHash.Initialize","ICertPropertyArchivedKeyHash::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","ICertPropertyArchivedKeyHash interface","certenroll/ICertPropertyArchivedKeyHash::Initialize","security.icertpropertyarchivedkeyhash_initialize_method"]
old-location: security\icertpropertyarchivedkeyhash_initialize_method.htm
tech.root: seccertenroll
ms.assetid: 1f201b37-6f3a-4f1c-83b8-2f1dbb1d4d07
ms.date: 12/05/2018
ms.keywords: ICertPropertyArchivedKeyHash interface [Security],Initialize method, ICertPropertyArchivedKeyHash.Initialize, ICertPropertyArchivedKeyHash::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyArchivedKeyHash interface, certenroll/ICertPropertyArchivedKeyHash::Initialize, security.icertpropertyarchivedkeyhash_initialize_method
f1_keywords:
- certenroll/ICertPropertyArchivedKeyHash.Initialize
dev_langs:
- c++
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
- ICertPropertyArchivedKeyHash.Initialize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertPropertyArchivedKeyHash::Initialize


## -description


The <b>Initialize</b> method initializes the object from a  byte array that contains the hash. The byte array is represented as a Unicode-encoded string.


## -parameters




### -param Encoding [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the input string.


### -param strArchivedKeyHashValue [in]

A <b>BSTR</b> variable that contains a SHA-1 hash of the encrypted private key.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

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



 Call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertproperty-setvalueoncertificate">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertpropertyarchivedkeyhash-get_archivedkeyhash">ArchivedKeyHash</a> property to retrieve the hash.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey">ArchivePrivateKey</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertpropertyarchivedkeyhash">ICertPropertyArchivedKeyHash</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate">KeyArchivalCertificate</a>
 

 

