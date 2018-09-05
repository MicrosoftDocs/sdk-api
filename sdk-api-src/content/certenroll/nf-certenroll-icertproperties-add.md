---
UID: NF:certenroll.ICertProperties.Add
title: ICertProperties::Add
author: windows-sdk-content
description: Adds a property to the collection.
old-location: security\icertproperties_add_method.htm
old-project: SecCertEnroll
ms.assetid: 53ea895d-0c41-445e-bfcc-2b2e53e10ff8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Add, Add method [Security], Add method [Security],ICertProperties interface, ICertProperties interface [Security],Add method, ICertProperties.Add, ICertProperties::Add, certenroll/ICertProperties::Add, security.icertproperties_add_method
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
 - ICertProperties.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICertProperties::Add


## -description


The <b>Add</b> method adds a property to the collection. This method is web enabled.


## -parameters




### -param pVal






#### - pValue [in]

Pointer to an <a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a> interface that represents the property to add to the collection.


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
<dt><b><b>HRESULT_FROM_WIN32(ERROR_FILE_EXISTS)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
An item in the collection has the same ID as the property you specified.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b830c0af-0a38-419d-8a33-8e3626c4e8f1">ICertProperties</a>



<a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>
 

 

