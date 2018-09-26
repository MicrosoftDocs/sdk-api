---
UID: NF:tapi3if.ITDispatchMapper.QueryDispatchInterface
title: ITDispatchMapper::QueryDispatchInterface
author: windows-sdk-content
description: The QueryDispatchInterface method returns a dispatch pointer to a different interface on an object given its GUID and the dispatch pointer of another interface on the object.
old-location: tapi3\itdispatchmapper_querydispatchinterface.htm
tech.root: tapi
ms.assetid: 7ee7c6f4-5710-4300-a2b8-de9aecf0528b
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ITDispatchMapper interface [TAPI 2.2],QueryDispatchInterface method, ITDispatchMapper.QueryDispatchInterface, ITDispatchMapper::QueryDispatchInterface, QueryDispatchInterface, QueryDispatchInterface method [TAPI 2.2], QueryDispatchInterface method [TAPI 2.2],ITDispatchMapper interface, _tapi3_itdispatchmapper_querydispatchinterface, tapi3.itdispatchmapper_querydispatchinterface, tapi3if/ITDispatchMapper::QueryDispatchInterface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITDispatchMapper.QueryDispatchInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITDispatchMapper::QueryDispatchInterface


## -description


The 
<b>QueryDispatchInterface</b> method returns a dispatch pointer to a different interface on an object given its GUID and the dispatch pointer of another interface on the object.


## -parameters




### -param pIID [in]

Pointer to <b>BSTR</b> representation of GUID for needed interface.


### -param pInterfaceToMap [in]

<b>IDispatch</b> pointer of starting interface.


### -param ppReturnedInterface [out]

<b>IDispatch</b> pointer of interface corresponding the GUID contained in <i>pIID</i>.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pIID</i> parameter either is not a valid BSTR or does not translate into a valid GUID.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The interface requested is not exposed or the object does not implement the <b>IObjectSafety</b> interface.

</td>
</tr>
</table>
 




## -remarks



The application must use 
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> to allocate memory for the <i>pIID</i> parameter and use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory when the variable is no longer needed.

The Dispatch Mapper will use the object's <b>IObjectSafety</b> interface to make sure the object is safe for scripting on the requested interface. If the object does not implement <b>IObjectSafety</b>, or if the object is not safe on this particular interface, the call will fail.




## -see-also




<a href="https://msdn.microsoft.com/65286ea6-b9a6-423b-9833-2d41ef2fd8de">ITDispatchMapper</a>
 

 

