---
UID: NF:certenroll.IX509Enrollment.InitializeFromTemplateName
title: IX509Enrollment::InitializeFromTemplateName
author: windows-sdk-content
description: Initializes the enrollment object from a template common name (CN).
old-location: security\ix509enrollment_initializefromtemplatename_method.htm
tech.root: SecCertEnroll
ms.assetid: 44a934f4-9ae9-4f52-9d44-f5fcf30f3837
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IX509Enrollment interface [Security],InitializeFromTemplateName method, IX509Enrollment.InitializeFromTemplateName, IX509Enrollment::InitializeFromTemplateName, InitializeFromTemplateName, InitializeFromTemplateName method [Security], InitializeFromTemplateName method [Security],IX509Enrollment interface, certenroll/IX509Enrollment::InitializeFromTemplateName, security.ix509enrollment_initializefromtemplatename_method
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
 - IX509Enrollment.InitializeFromTemplateName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509Enrollment::InitializeFromTemplateName


## -description


The <b>InitializeFromTemplateName</b> method initializes the enrollment object from a template common name (CN).


## -parameters




### -param Context [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa379399(v=VS.85).aspx">X509CertificateEnrollmentContext</a> enumeration value that indicates whether the requested enrollment is for a user, a computer, or an administrator acting on behalf of a computer.


### -param strTemplateName [in]

A  <b>BSTR</b> variable that contains the Common Name (CN) of the template as it appears in Active Directory or the dotted decimal <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a>.


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



The <b>InitializeFromTemplateName</b> method:

<ul>
<li>Examines the template to determine the type of request needed.</li>
<li>Creates the appropriate type of request object (PKCS #10, PKCS #7, or CMC).</li>
<li>Sets the following properties on the request if values currently exist:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377643(v=VS.85).aspx">CspInformations</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377677(v=VS.85).aspx">ParentWindow</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377696(v=VS.85).aspx">Silent</a>
</li>
</ul>
</li>
<li>Initializes the request object by using the template.</li>
<li>Retrieves the signature count, issuance policies, and application policies from the template.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a>
 

 

