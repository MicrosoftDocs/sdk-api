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

# ITCollection::get__NewEnum


## -description


The 
<b>get__NewEnum</b> method gets an enumerator for the collection.


## -parameters




### -param ppNewEnum [out]

Pointer to an 
<a href="_com_iunknown">IUnknown</a> interface on an enumerator object for the collection. 




Call the 
<a href="_com_iunknown_queryinterface">QueryInterface</a> method on the returned <b>IUnknown</b> interface to obtain a pointer to an 
<a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> enumeration interface on the collection. <b>IEnumVARIANT</b> provides a number of methods that you can use to iterate through the collection.

For more information, see the following Remarks section.


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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -remarks



Each TAPI 3 interface that includes a method that returns a collection also includes a method that returns a pointer to a TAPI 3 enumerator interface. If you are programming in C/C++, it can be easier to call a collection's enumerator method directly to obtain an enumerator object, instead of calling the <b>ITCollection::get__NewEnum</b> method. For example, the 
<a href="https://msdn.microsoft.com/b40a2071-24bf-470c-bfba-de23317e8652">ITTAPI::EnumerateAddresses</a> method returns a pointer to an 
<a href="https://msdn.microsoft.com/bfe9f12e-ceb7-4120-8193-70feb2bc7c85">IEnumAddress</a> interface. 
<b>IEnumAddress</b> provides enumeration methods for the 
<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address object</a>.

If you are programming in Visual Basic, you do not need to call this method to enumerate a collection. This is because you can invoke the method's functionality implicitly using the <b>For...Each...in...Next...</b> construct.




## -see-also




<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a>
 

 

