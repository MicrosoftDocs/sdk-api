---
UID: NF:certenroll.ICertPropertyAutoEnroll.Initialize
title: ICertPropertyAutoEnroll::Initialize
author: windows-sdk-content
description: Initializes the object by specifying the name of the template to be used for autoenrollment.
old-location: security\icertpropertyautoenroll_initialize_method.htm
old-project: seccertenroll
ms.assetid: f9a949c8-acd9-45b2-882e-84daf0acfad4
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ICertPropertyAutoEnroll interface [Security],Initialize method, ICertPropertyAutoEnroll.Initialize, ICertPropertyAutoEnroll::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyAutoEnroll interface, certenroll/ICertPropertyAutoEnroll::Initialize, security.icertpropertyautoenroll_initialize_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
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
 - ICertPropertyAutoEnroll.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICertPropertyAutoEnroll::Initialize


## -description


The <b>Initialize</b> method initializes the object by specifying the name of the template to be used for autoenrollment.


## -parameters




### -param strTemplateName [in]

A <b>BSTR</b> variable that contains the template name or object identifier.


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



 Call the <a href="https://msdn.microsoft.com/en-us/library/Aa375928(v=VS.85).aspx">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="https://msdn.microsoft.com/en-us/library/Aa375253(v=VS.85).aspx">TemplateName</a> property to retrieve the template name.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375239(v=VS.85).aspx">ICertProperty</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375250(v=VS.85).aspx">ICertPropertyAutoEnroll</a>
 

 

