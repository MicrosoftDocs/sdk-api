---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ITypeInfo::CreateInstance


## -description


Creates a new instance of a type that describes a component object class (coclass).


## -parameters




### -param pUnkOuter [in]

The controlling <b>IUnknown</b>. If Null, then a stand-alone instance is created. If valid, then an aggregate object is created.


### -param riid [in]

An ID for the interface that the caller will use to communicate with the resulting object.




### -param ppvObj [out]

An instance of the created object.


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK
</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
OLE could not find an implementation of one or more required interfaces.

</td>
</tr>
</table>
 

Additional errors may be returned from <a href="https://msdn.microsoft.com/a276e30c-6a7f-4cde-9639-21a9f5170b62">GetActiveObject</a> or <b>CoCreateInstance</b>.




## -remarks



For types that describe a component object class (coclass), <b>CreateInstance</b> creates a new instance of the class. Normally, <b>CreateInstance</b> calls <b>CoCreateInstance</b> with the type description's GUID. For an Application object, it first calls <a href="https://msdn.microsoft.com/a276e30c-6a7f-4cde-9639-21a9f5170b62">GetActiveObject</a>. If the application is active, <b>GetActiveObject</b> returns the active object; otherwise, if <b>GetActiveObject</b> fails, <b>CreateInstance</b> calls <b>CoCreateInstance</b>.





## -see-also




<a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a>
 

 

