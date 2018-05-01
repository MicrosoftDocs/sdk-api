---
UID: NF:certenroll.IX509Enrollment.Enroll
title: IX509Enrollment::Enroll method
author: windows-driver-content
description: Encodes a request, submits it to an appropriate certification authority (CA), and installs the response.
old-location: security\ix509enrollment_enroll_method.htm
old-project: SecCertEnroll
ms.assetid: 63abecac-39f4-497a-8851-7a2260abc3dd
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: Enroll method [Security], Enroll method [Security], IX509Enrollment interface, Enroll,IX509Enrollment.Enroll, IX509Enrollment, IX509Enrollment interface [Security], Enroll method, IX509Enrollment::Enroll, certenroll/IX509Enrollment::Enroll, security.ix509enrollment_enroll_method
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
-	IX509Enrollment.Enroll
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509Enrollment::Enroll method


## -description


The <b>Enroll</b> method encodes a request, submits it to an appropriate certification authority (CA), and installs the response.


## -parameters






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
<dt><b><b>OLE_E_BLANK</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The enrollment object has not been initialized.

</td>
</tr>
</table>
 




## -remarks



The method may create a key pair if necessary. Depending on how you initialize the enrollment object and on what properties you set, there may be no need to create a key pair. For example, if you are renewing a certificate by using an existing key, or if the <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> object associated with the certificate request represents an existing key, this method does not create a new key pair.

Before enrolling, you must initialize the <a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a> object by calling one of the following methods.<ul>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/04cb00af-f786-4548-bee3-2cc5083278c3">InitializeFromRequest</a>
</li>
<li>
<a href="https://msdn.microsoft.com/44a934f4-9ae9-4f52-9d44-f5fcf30f3837">InitializeFromTemplateName</a>
</li>
</ul>


If the enrollment operation succeeds, the function  returns <b>S_OK</b>. However, this does not necessarily mean that the response from the CA was installed. Call  the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> property to determine the enrollment status.




## -see-also




<a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a>
 

 

