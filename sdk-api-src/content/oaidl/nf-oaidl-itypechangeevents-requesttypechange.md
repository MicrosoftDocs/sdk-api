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

# ITypeChangeEvents::RequestTypeChange


## -description


Raised when a request has been made to change a type. The change can be disallowed.


## -parameters




### -param changeKind [in]

The type of change.

<a id="CHANGEKIND_ADDMEMBER"></a>
<a id="changekind_addmember"></a>


#### CHANGEKIND_ADDMEMBER

<a id="CHANGEKIND_DELETEMEMBER"></a>
<a id="changekind_deletemember"></a>


#### CHANGEKIND_DELETEMEMBER

<a id="CHANGEKIND_SETNAMES"></a>
<a id="changekind_setnames"></a>


#### CHANGEKIND_SETNAMES

<a id="CHANGEKIND_SETDOCUMENTATION"></a>
<a id="changekind_setdocumentation"></a>


#### CHANGEKIND_SETDOCUMENTATION

<a id="CHANGEKIND_GENERAL"></a>
<a id="changekind_general"></a>


#### CHANGEKIND_GENERAL

<a id="CHANGEKIND_INVALIDATE"></a>
<a id="changekind_invalidate"></a>


#### CHANGEKIND_INVALIDATE

<a id="CHANGEKIND_CHANGEFAILED"></a>
<a id="changekind_changefailed"></a>


#### CHANGEKIND_CHANGEFAILED


### -param pTInfoBefore [in]

An object that implements the <a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a>, <a href="https://msdn.microsoft.com/d3a34a13-6114-4f15-9de5-60da43fde600">ITypeInfo2</a>, <a href="https://msdn.microsoft.com/c8bbb677-2666-4900-8fb9-788742eef656">ICreateTypeInfo</a>, or <a href="https://msdn.microsoft.com/34dc6f52-6864-4edb-b22d-80eef05d4c8c">ICreateTypeInfo2</a> interface and that contains the type information before the change was made. The client subscribes to this object to receive notifications about any changes. 



### -param pStrName [in]

The name of the change. This value may be null.


### -param pfCancel [out]

False to disallow the change; otherwise, true.



## -returns



This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5e286a4b-b36b-40d6-9a39-d572086e5a2d">ITypeChangeEvents</a>
 

 

