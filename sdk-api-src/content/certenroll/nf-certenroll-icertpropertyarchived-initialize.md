---
UID: NF:certenroll.ICertPropertyArchived.Initialize
title: ICertPropertyArchived::Initialize
author: windows-sdk-content
description: Initializes the object from a Boolean value that specifies whether the certificate has been archived.
old-location: security\icertpropertyarchived_initialize_method.htm
old-project: SecCertEnroll
ms.assetid: 66efee4f-61af-447a-b668-81fbe2107b7f
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ICertPropertyArchived interface [Security],Initialize method, ICertPropertyArchived.Initialize, ICertPropertyArchived::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyArchived interface, certenroll/ICertPropertyArchived::Initialize, security.icertpropertyarchived_initialize_method
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	ICertPropertyArchived.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICertPropertyArchived::Initialize


## -description


The <b>Initialize</b> method initializes the object from a Boolean value that specifies whether the certificate has been archived.


## -parameters




### -param ArchivedValue [in]

A <b>VARIANT_BOOL</b> variable that identifies whether the certificate has been archived.


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



 Call the <a href="https://msdn.microsoft.com/46c409c4-46bd-4349-8363-1983f4411bc2">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="https://msdn.microsoft.com/c4154d9e-5a37-4a6c-9fc3-5935d8c54dc4">Archived</a> property to retrieve the Boolean value.




## -see-also




<a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>



<a href="https://msdn.microsoft.com/81219ad9-4717-40e5-9ecd-d3df980e23c6">ICertPropertyArchived</a>
 

 

