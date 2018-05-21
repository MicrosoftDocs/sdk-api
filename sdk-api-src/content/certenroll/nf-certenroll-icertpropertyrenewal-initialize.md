---
UID: NF:certenroll.ICertPropertyRenewal.Initialize
title: ICertPropertyRenewal::Initialize
author: windows-driver-content
description: Initializes the object from a SHA-1 hash of the new certificate.
old-location: security\icertpropertyrenewal_initialize_method.htm
old-project: SecCertEnroll
ms.assetid: dc1e124e-400a-4f1e-8e87-095b6a3341d4
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: ICertPropertyRenewal interface [Security],Initialize method, ICertPropertyRenewal.Initialize, ICertPropertyRenewal::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyRenewal interface, certenroll/ICertPropertyRenewal::Initialize, security.icertpropertyrenewal_initialize_method
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
-	ICertPropertyRenewal.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICertPropertyRenewal::Initialize


## -description


The <b>Initialize</b> method initializes the object from a SHA-1 hash of the new certificate.


## -parameters




### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the input string that contains the hash.


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



Typically this property is initialized during the enrollment process. You can retrieve the certificate used during enrollment by calling the <a href="https://msdn.microsoft.com/636e4c6d-38b9-4a27-b640-4c071816ee97">Certificate</a> property on the <a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a> interface.

Call the <a href="https://msdn.microsoft.com/46c409c4-46bd-4349-8363-1983f4411bc2">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="https://msdn.microsoft.com/f2ea8198-01ec-4485-9f7e-9b9fa8ddba6f">Renewal</a> property to retrieve the hash.




## -see-also




<a href="https://msdn.microsoft.com/c87a391a-aec9-4b42-8084-c593ecbb0bc6">ICertPropertyRenewal</a>
 

 

