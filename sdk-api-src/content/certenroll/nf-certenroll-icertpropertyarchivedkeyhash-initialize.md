---
UID: NF:certenroll.ICertPropertyArchivedKeyHash.Initialize
title: ICertPropertyArchivedKeyHash::Initialize
author: windows-sdk-content
description: Initializes the object from a byte array that contains the hash.
old-location: security\icertpropertyarchivedkeyhash_initialize_method.htm
tech.root: seccertenroll
ms.assetid: 1f201b37-6f3a-4f1c-83b8-2f1dbb1d4d07
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ICertPropertyArchivedKeyHash interface [Security],Initialize method, ICertPropertyArchivedKeyHash.Initialize, ICertPropertyArchivedKeyHash::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyArchivedKeyHash interface, certenroll/ICertPropertyArchivedKeyHash::Initialize, security.icertpropertyarchivedkeyhash_initialize_method
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

An <a href="https://msdn.microsoft.com/en-us/library/Aa374936(v=VS.85).aspx">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the input string.


### -param strArchivedKeyHashValue [in]

A <b>BSTR</b> variable that contains a SHA-1 hash of the encrypted private key.


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



 Call the <a href="https://msdn.microsoft.com/en-us/library/Aa375928(v=VS.85).aspx">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="https://msdn.microsoft.com/en-us/library/Aa375242(v=VS.85).aspx">ArchivedKeyHash</a> property to retrieve the hash.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377134(v=VS.85).aspx">ArchivePrivateKey</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375241(v=VS.85).aspx">ICertPropertyArchivedKeyHash</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377262(v=VS.85).aspx">KeyArchivalCertificate</a>
 

 

