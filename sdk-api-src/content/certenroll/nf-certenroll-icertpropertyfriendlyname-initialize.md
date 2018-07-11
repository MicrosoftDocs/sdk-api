---
UID: NF:certenroll.ICertPropertyFriendlyName.Initialize
title: ICertPropertyFriendlyName::Initialize
author: windows-sdk-content
description: Initializes the object from the certificate display name.
old-location: security\icertpropertyfriendlyname_initialize_method.htm
old-project: seccertenroll
ms.assetid: fb9a8108-f3d1-4a5c-bf3f-00002c085012
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: ICertPropertyFriendlyName interface [Security],Initialize method, ICertPropertyFriendlyName.Initialize, ICertPropertyFriendlyName::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyFriendlyName interface, certenroll/ICertPropertyFriendlyName::Initialize, security.icertpropertyfriendlyname_initialize_method
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICertPropertyFriendlyName.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICertPropertyFriendlyName::Initialize


## -description


The <b>Initialize</b> method initializes the object from the certificate display name. This method is web enabled.


## -parameters




### -param strFriendlyName [in]

A <b>BSTR</b> variable that contains the name.  The string length cannot exceed 260 characters.


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
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32(ERROR_FILENAME_EXCED_RANGE)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The string length exceeds 260 characters.

</td>
</tr>
</table>
 




## -remarks



Typically, you specify the display name in a user interface or from the command line before beginning the enrollment process so that the name can be associated with the dummy certificate in the request store. To retrieve that value and use it here, call the <a href="https://msdn.microsoft.com/35c3eea1-2a3a-4e13-9232-f40429669948">CertificateFriendlyName</a> on the <a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a> interface.

Call the <a href="https://msdn.microsoft.com/46c409c4-46bd-4349-8363-1983f4411bc2">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="https://msdn.microsoft.com/7204800e-e7ae-4fc0-a221-d6f3c2b2855b">FriendlyName</a> property to retrieve the display name.




## -see-also




<a href="https://msdn.microsoft.com/b830c0af-0a38-419d-8a33-8e3626c4e8f1">ICertProperties</a>



<a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>



<a href="https://msdn.microsoft.com/229e8ce9-fe18-45f4-8f91-cd741052a134">ICertPropertyDescription</a>



<a href="https://msdn.microsoft.com/d2bfe2f2-423e-4620-8933-bbae4f98c62a">ICertPropertyFriendlyName</a>
 

 

