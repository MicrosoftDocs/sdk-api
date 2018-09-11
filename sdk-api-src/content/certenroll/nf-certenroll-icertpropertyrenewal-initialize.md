---
UID: NF:certenroll.ICertPropertyRenewal.Initialize
title: ICertPropertyRenewal::Initialize
author: windows-sdk-content
description: Initializes the object from a SHA-1 hash of the new certificate.
old-location: security\icertpropertyrenewal_initialize_method.htm
tech.root: SecCertEnroll
ms.assetid: dc1e124e-400a-4f1e-8e87-095b6a3341d4
ms.author: windowssdkdev
ms.date: 08/29/2018
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
 - ICertPropertyRenewal.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertPropertyRenewal::Initialize


## -description


The <b>Initialize</b> method initializes the object from a SHA-1 hash of the new certificate.


## -parameters




### -param Encoding [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa374936(v=VS.85).aspx">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the input string that contains the hash.


### -param strRenewalValue [in]

A <b>BSTR</b> variable that contains the hash.


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



Typically this property is initialized during the enrollment process. You can retrieve the certificate used during enrollment by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa377867(v=VS.85).aspx">Certificate</a> property on the <a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a> interface.

Call the <a href="https://msdn.microsoft.com/en-us/library/Aa375928(v=VS.85).aspx">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="https://msdn.microsoft.com/en-us/library/Aa375766(v=VS.85).aspx">Renewal</a> property to retrieve the hash.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375749(v=VS.85).aspx">ICertPropertyRenewal</a>
 

 

