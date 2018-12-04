---
UID: NF:certenroll.ICertPropertyEnrollment.Initialize
title: ICertPropertyEnrollment::Initialize
author: windows-sdk-content
description: Initializes the property from the certificate request ID, the certification authority (CA) configuration string, and an optional certificate display name.
old-location: security\icertpropertyenrollment_initialize_method.htm
tech.root: seccertenroll
ms.assetid: 47e9b11f-3f23-4e2f-817a-4b6311e3d710
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ICertPropertyEnrollment interface [Security],Initialize method, ICertPropertyEnrollment.Initialize, ICertPropertyEnrollment::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyEnrollment interface, certenroll/ICertPropertyEnrollment::Initialize, security.icertpropertyenrollment_initialize_method
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
 - ICertPropertyEnrollment.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertPropertyEnrollment::Initialize


## -description


The <b>Initialize</b> method initializes the property from the certificate request ID, the certification authority (CA) configuration string, and an optional certificate display name.


## -parameters




### -param RequestId [in]

A <b>LONG</b> variable that contains the certificate request ID. A request ID is created by the enrollment process. You can retrieve this value by calling the <a href="https://msdn.microsoft.com/64048d5d-36fd-4709-a924-7f84a2b2b97e">RequestId</a> property on the <a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a> interface.


### -param strCADnsName [in]

A <b>BSTR</b> variable that contains the Domain Name System (DNS) name of the CA. This is the first name in the <i>CADnsName\CAName</i> CA configuration string. The configuration string is typically set during the enrollment process. The DNS name can be retrieved by calling the <a href="https://msdn.microsoft.com/4a4478c8-a665-4ee1-9f3a-cad259e1c9ce">CAConfigString</a> property and separating the  string into its constituent parts.


### -param strCAName [in]

A <b>BSTR</b> variable that contains the subject common name (CN) of the CA. This is the second name in the <i>CADnsName\CAName</i> CA configuration string. The configuration string is typically set during the enrollment process. The CN name can be retrieved by calling the <a href="https://msdn.microsoft.com/4a4478c8-a665-4ee1-9f3a-cad259e1c9ce">CAConfigString</a> property and separating the  string into its constituent parts.


### -param strFriendlyName [in, optional]

A <b>BSTR</b> variable that contains an optional display name for the certificate. The default value is <b>NULL</b>. This value is typically set during the enrollment process. You can retrieve it by calling the <a href="https://msdn.microsoft.com/35c3eea1-2a3a-4e13-9232-f40429669948">CertificateFriendlyName</a> property.


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



The values that you can use to initialize the <a href="https://msdn.microsoft.com/7530998b-b59c-426b-a74a-ead4bca55c3b">ICertPropertyEnrollment</a> object are set during the certificate enrollment process when the client calls the <a href="https://msdn.microsoft.com/63abecac-39f4-497a-8851-7a2260abc3dd">Enroll</a> method on the <a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a> object. That is, to retrieve a request ID, call the <a href="https://msdn.microsoft.com/64048d5d-36fd-4709-a924-7f84a2b2b97e">RequestId</a> property on the <b>IX509Enrollment</b> object. To retrieve a certificate display name, call the <a href="https://msdn.microsoft.com/35c3eea1-2a3a-4e13-9232-f40429669948">CertificateFriendlyName</a> property. To retrieve a distinguished name and common name, call the <a href="https://msdn.microsoft.com/4a4478c8-a665-4ee1-9f3a-cad259e1c9ce">CAConfigString</a> property and separate the configuration string into its constituent parts.

Call the <a href="https://msdn.microsoft.com/46c409c4-46bd-4349-8363-1983f4411bc2">SetValueOnCertificate</a> method to associate the property with a certificate. You can also call the following properties to retrieve the values specified during initialization:<ul>
<li>
<a href="https://msdn.microsoft.com/5b388cfe-e0b1-4b57-bf6c-81f9ab65ffcf">CADnsName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ea490e37-e1b9-4887-8051-c3447136875c">CAName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a12b7368-cace-47c4-bfd4-08845dc2634c">FriendlyName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a9e2000c-7d64-43f1-b891-b5cd6f46201f">RequestId</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>



<a href="https://msdn.microsoft.com/7530998b-b59c-426b-a74a-ead4bca55c3b">ICertPropertyEnrollment</a>
 

 

