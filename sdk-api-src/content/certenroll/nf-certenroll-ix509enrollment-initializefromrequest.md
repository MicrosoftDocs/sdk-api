---
UID: NF:certenroll.IX509Enrollment.InitializeFromRequest
title: IX509Enrollment::InitializeFromRequest
author: windows-sdk-content
description: Initializes the enrollment object from an existing IX509CertificateRequest object.
old-location: security\ix509enrollment_initializefromrequest_method.htm
tech.root: SecCertEnroll
ms.assetid: 04cb00af-f786-4548-bee3-2cc5083278c3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509Enrollment interface [Security],InitializeFromRequest method, IX509Enrollment.InitializeFromRequest, IX509Enrollment::InitializeFromRequest, InitializeFromRequest, InitializeFromRequest method [Security], InitializeFromRequest method [Security],IX509Enrollment interface, certenroll/IX509Enrollment::InitializeFromRequest, security.ix509enrollment_initializefromrequest_method
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
 - IX509Enrollment.InitializeFromRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509Enrollment::InitializeFromRequest


## -description


The <b>InitializeFromRequest</b> method initializes the enrollment object from an existing <a href="https://msdn.microsoft.com/en-us/library/Aa377123(v=VS.85).aspx">IX509CertificateRequest</a> object. This method is web enabled.


## -parameters




### -param pRequest [in]

Pointer to the <a href="https://msdn.microsoft.com/en-us/library/Aa377123(v=VS.85).aspx">IX509CertificateRequest</a> interface.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

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
The enrollment object has already been initialized.

</td>
</tr>
</table>
 




## -remarks



The <b>InitializeFromRequest</b>  method:

<ul>
<li>Verifies that the request is a PKCS #10, PKCS #7, or CMC request object.</li>
<li>Retrieves the template, if any, associated with the request.</li>
<li>Validates the template.</li>
<li>Sets the request object on the <a href="https://msdn.microsoft.com/en-us/library/Aa378069(v=VS.85).aspx">Request</a> property.</li>
<li>Retrieves the signature count, issuance policies, and application policies from the template.</li>
<li>Retrieves the renewal certificate if one exists.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377123(v=VS.85).aspx">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a>
 

 

