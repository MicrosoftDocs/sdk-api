---
UID: NF:certenroll.ICertPropertyDescription.Initialize
title: ICertPropertyDescription::Initialize (certenroll.h)
author: windows-sdk-content
description: Initializes the object from a string that contains descriptive information about the certificate.
old-location: security\icertpropertydescription_initialize_method.htm
tech.root: seccertenroll
ms.assetid: 17e8ee9c-c861-4437-a70d-ccad6a5a293d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICertPropertyDescription interface [Security],Initialize method, ICertPropertyDescription.Initialize, ICertPropertyDescription::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyDescription interface, certenroll/ICertPropertyDescription::Initialize, security.icertpropertydescription_initialize_method
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
 - ICertPropertyDescription.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertPropertyDescription::Initialize


## -description


The <b>Initialize</b> method initializes the object from a string that contains descriptive information about the certificate. Use this property to create a string that can be displayed in user interfaces that enumerate certificate properties. This method is web enabled.


## -parameters




### -param strDescription [in]

A <b>BSTR</b> variable that contains a description. The string length cannot exceed 260 characters.


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



Call the <a href="https://msdn.microsoft.com/46c409c4-46bd-4349-8363-1983f4411bc2">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="https://msdn.microsoft.com/afc8c4f4-186b-4f00-b12b-54b50913865d">Description</a> property to retrieve the description string.




## -see-also




<a href="https://msdn.microsoft.com/b830c0af-0a38-419d-8a33-8e3626c4e8f1">ICertProperties</a>



<a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>



<a href="https://msdn.microsoft.com/229e8ce9-fe18-45f4-8f91-cd741052a134">ICertPropertyDescription</a>



<a href="https://msdn.microsoft.com/d2bfe2f2-423e-4620-8933-bbae4f98c62a">ICertPropertyFriendlyName</a>
 

 

