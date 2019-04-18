---
UID: NF:ocidl.IPersistStreamInit.InitNew
title: IPersistStreamInit::InitNew (ocidl.h)
author: windows-sdk-content
description: Initializes an object to a default state. This method is to be called instead of IPersistStreamInit::Load.
old-location: com\ipersiststreaminit_initnew.htm
tech.root: com
ms.assetid: 9e318698-0c3c-41c2-bb9e-04e8c9746c4d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPersistStreamInit interface [COM],InitNew method, IPersistStreamInit.InitNew, IPersistStreamInit::InitNew, InitNew, InitNew method [COM], InitNew method [COM],IPersistStreamInit interface, _com_ipersiststreaminit_initnew, com.ipersiststreaminit_initnew, ocidl/IPersistStreamInit::InitNew
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPersistStreamInit.InitNew
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPersistStreamInit::InitNew


## -description


Initializes an object to a default state. This method is to be called instead of <a href="https://msdn.microsoft.com/3e995e07-e088-40de-ba28-c30caea45786">IPersistStreamInit::Load</a>.


## -parameters






## -returns



This method can return the standard return valuesE_OUTOFMEMORY and E_UNEXPECTED, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The object requires no default initialization. This error code is allowed because an object may choose to implement <a href="https://msdn.microsoft.com/49c413b3-3523-4602-9ec1-19f4e0fe5651">IPersistStreamInit</a> simply for orthogonality or in anticipation of a future need for this method.

</td>
</tr>
</table>
 




## -remarks



If the object has already been initialized with <a href="https://msdn.microsoft.com/3e995e07-e088-40de-ba28-c30caea45786">IPersistStreamInit::Load</a>, then this method must return E_UNEXPECTED.




## -see-also




<a href="https://msdn.microsoft.com/49c413b3-3523-4602-9ec1-19f4e0fe5651">IPersistStreamInit</a>
 

 

