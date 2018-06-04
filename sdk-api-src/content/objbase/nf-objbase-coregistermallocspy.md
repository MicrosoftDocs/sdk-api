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

# CoRegisterMallocSpy function


## -description


Registers an implementation of the <a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a> interface, thereafter requiring OLE to call its wrapper methods around every call to the corresponding <a href="https://msdn.microsoft.com/047f281e-2665-4d6d-9a0b-918cd3339447">IMalloc</a> method. 


## -parameters




### -param pMallocSpy [in]

A pointer to an instance of the <a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a> implementation.


## -returns



This function can return the standard return value E_INVALIDARG, as well as the following values.

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
The object was successfully registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_OBJISREG</b></dt>
</dl>
</td>
<td width="60%">
The object is already registered.

</td>
</tr>
</table>
 




## -remarks



The <b>CoRegisterMallocSpy</b> function registers the <a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a> object, which is used to debug calls to <a href="https://msdn.microsoft.com/047f281e-2665-4d6d-9a0b-918cd3339447">IMalloc</a> methods. The function calls <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the pointer <i>pMallocSpy</i> for the interface IID_IMallocSpy. This is to ensure that <i>pMallocSpy</i> really points to an implementation of <b>IMallocSpy</b>. By the rules of OLE, it is expected that a successful call to <b>QueryInterface</b> has added a reference (through the <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> method) to the <b>IMallocSpy</b> object. That is, <b>CoRegisterMallocSpy</b> does not directly call <b>AddRef</b> on <i>pMallocSpy</i>, but fully expects that the <b>QueryInterface</b> call will.



When the <a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a> object is registered, whenever there is a call to one of the <a href="https://msdn.microsoft.com/047f281e-2665-4d6d-9a0b-918cd3339447">IMalloc</a> methods, OLE first calls the corresponding <b>IMallocSpy</b> pre-method. Then, after executing the <b>IMalloc</b> method, OLE calls the corresponding <b>IMallocSpy</b> post-method. For example, whenever there is a call to <a href="https://msdn.microsoft.com/c9c9bdac-965f-4b18-9338-28a025930480">IMalloc::Alloc</a>, from whatever source, OLE calls <a href="https://msdn.microsoft.com/43d8223b-a3fb-432c-ab4e-009d79ad8658">IMallocSpy::PreAlloc</a>, calls <b>Alloc</b>, and after that allocation is completed, calls <a href="https://msdn.microsoft.com/eaf2cb92-afdb-4f1f-a46a-83b6c72db07f">IMallocSpy::PostAlloc</a>.





## -see-also




<a href="https://msdn.microsoft.com/d1d09fbe-ca5c-4480-b807-3afcc043ccb9">CoGetMalloc</a>



<a href="https://msdn.microsoft.com/e1e984a2-2aee-452c-840c-42201ef5ee96">CoRevokeMallocSpy</a>



<a href="https://msdn.microsoft.com/8ba500f7-c070-4788-b7fe-58b6a4e6a94c">IMallocSpy</a>
 

 

