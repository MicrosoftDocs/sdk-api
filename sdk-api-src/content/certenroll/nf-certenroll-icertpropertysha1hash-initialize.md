---
UID: NF:certenroll.ICertPropertySHA1Hash.Initialize
title: ICertPropertySHA1Hash::Initialize
author: windows-sdk-content
description: Initializes the object from the SHA-1 hash of a certificate.
old-location: security\icertpropertysha1hash_initialize_method.htm
old-project: SecCertEnroll
ms.assetid: 898da01b-94e6-4a07-9c53-f93378fbda8c
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ICertPropertySHA1Hash interface [Security],Initialize method, ICertPropertySHA1Hash.Initialize, ICertPropertySHA1Hash::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertySHA1Hash interface, certenroll/ICertPropertySHA1Hash::Initialize, security.icertpropertysha1hash_initialize_method
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	ICertPropertySHA1Hash.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICertPropertySHA1Hash::Initialize


## -description


The <b>Initialize</b> method initializes the object from the SHA-1 hash of a certificate.


## -parameters




### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the input string that contains the certificate hash.


### -param strRenewalValue [in]

A <b>BSTR</b> variable that contains the hash.


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



Call the <a href="https://msdn.microsoft.com/46c409c4-46bd-4349-8363-1983f4411bc2">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="https://msdn.microsoft.com/28c6efb3-1cf7-4f3b-ad42-6f5d72d3117b">SHA1Hash</a> property to retrieve the hash value.




## -see-also




<a href="https://msdn.microsoft.com/0946827b-c933-472c-9466-aaa3495ab202">ICertPropertySHA1Hash</a>
 

 

