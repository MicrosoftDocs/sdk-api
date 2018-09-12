---
UID: NF:certenroll.ICertPropertyAutoEnroll.Initialize
title: ICertPropertyAutoEnroll::Initialize
author: windows-sdk-content
description: Initializes the object by specifying the name of the template to be used for autoenrollment.
old-location: security\icertpropertyautoenroll_initialize_method.htm
tech.root: SecCertEnroll
ms.assetid: f9a949c8-acd9-45b2-882e-84daf0acfad4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ICertPropertyAutoEnroll interface [Security],Initialize method, ICertPropertyAutoEnroll.Initialize, ICertPropertyAutoEnroll::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyAutoEnroll interface, certenroll/ICertPropertyAutoEnroll::Initialize, security.icertpropertyautoenroll_initialize_method
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
 - ICertPropertyAutoEnroll.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertPropertyAutoEnroll::Initialize


## -description


The <b>Initialize</b> method initializes the object by specifying the name of the template to be used for autoenrollment.


## -parameters




### -param strTemplateName [in]

A <b>BSTR</b> variable that contains the template name or object identifier.


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



 Call the <a href="https://msdn.microsoft.com/46c409c4-46bd-4349-8363-1983f4411bc2">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="https://msdn.microsoft.com/bec4be81-ff39-4517-be17-e5ca6f0b08e9">TemplateName</a> property to retrieve the template name.




## -see-also




<a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>



<a href="https://msdn.microsoft.com/25eab0e9-4980-49ad-9d3b-35ad47c20bcb">ICertPropertyAutoEnroll</a>
 

 

