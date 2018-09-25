---
UID: NF:objbase.CoRegisterMallocSpy
title: CoRegisterMallocSpy function
author: windows-sdk-content
description: Registers an implementation of the IMallocSpy interface, thereafter requiring OLE to call its wrapper methods around every call to the corresponding IMalloc method.
old-location: com\coregistermallocspy.htm
tech.root: com
ms.assetid: 28623c1f-e158-4cc5-8c7f-c13d7a65aa76
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: CoRegisterMallocSpy, CoRegisterMallocSpy function [COM], _com_CoRegisterMallocSpy, com.coregistermallocspy, objbase/CoRegisterMallocSpy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-private-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-COM-Private-l1-1-1.dll
api_name:
 - CoRegisterMallocSpy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

