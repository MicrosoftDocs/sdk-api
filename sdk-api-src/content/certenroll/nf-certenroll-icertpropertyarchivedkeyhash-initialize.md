---
UID: NF:certenroll.ICertPropertyArchivedKeyHash.Initialize
title: ICertPropertyArchivedKeyHash::Initialize (certenroll.h)
author: windows-sdk-content
description: Initializes the object from a byte array that contains the hash.
old-location: security\icertpropertyarchivedkeyhash_initialize_method.htm
tech.root: seccertenroll
ms.assetid: 1f201b37-6f3a-4f1c-83b8-2f1dbb1d4d07
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICertPropertyArchivedKeyHash interface [Security],Initialize method, ICertPropertyArchivedKeyHash.Initialize, ICertPropertyArchivedKeyHash::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyArchivedKeyHash interface, certenroll/ICertPropertyArchivedKeyHash::Initialize, security.icertpropertyarchivedkeyhash_initialize_method
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
 - ICertPropertyArchivedKeyHash.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertPropertyArchivedKeyHash::Initialize


## -description


The <b>Initialize</b> method initializes the object from a  byte array that contains the hash. The byte array is represented as a Unicode-encoded string.


## -parameters




### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the input string.


### -param strArchivedKeyHashValue [in]

A <b>BSTR</b> variable that contains a SHA-1 hash of the encrypted private key.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

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



 Call the <a href="https://msdn.microsoft.com/46c409c4-46bd-4349-8363-1983f4411bc2">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="https://msdn.microsoft.com/b5f38bfc-58aa-42c6-a457-44bdfd013ce7">ArchivedKeyHash</a> property to retrieve the hash.




## -see-also




<a href="https://msdn.microsoft.com/6d17222e-3657-4911-a8e7-d90214284441">ArchivePrivateKey</a>



<a href="https://msdn.microsoft.com/06696346-b9d1-4229-991e-539862cff3c9">ICertPropertyArchivedKeyHash</a>



<a href="https://msdn.microsoft.com/93f71fd7-33bb-4352-b184-7270bca1363f">KeyArchivalCertificate</a>
 

 

