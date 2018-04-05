---
UID: NF:functiondiscoveryapi.IFunctionInstanceCollection.Get
title: IFunctionInstanceCollection::Get method
author: windows-driver-content
description: Gets the specified function instance and its index from the collection.
old-location: ncd\ifunctioninstancecollection_get.htm
old-project: FunDisc
ms.assetid: 3f3db880-a765-4a18-91ac-d091728cbb39
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Get method, Get method, IFunctionInstanceCollection interface, Get,IFunctionInstanceCollection.Get, IFunctionInstanceCollection, IFunctionInstanceCollection interface, Get method, IFunctionInstanceCollection::Get, functiondiscoveryapi/IFunctionInstanceCollection::Get, ncd.ifunctioninstancecollection_get
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: functiondiscoveryapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SystemVisibilityFlags
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FunDisc.dll
api_name:
-	IFunctionInstanceCollection.Get
product: Windows
targetos: Windows
req.lib: 
req.dll: FunDisc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFunctionInstanceCollection::Get method


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the specified function instance and its index from the collection.


## -parameters




### -param pszInstanceIdentity [in]

The identifier of the function instance to be retrieved (see <a href="https://msdn.microsoft.com/library/windows/hardware/ff546827">GetID</a>).


### -param pdwIndex [out]

The index number.


### -param ppIFunctionInstance [out]

 A pointer to an <a href="https://msdn.microsoft.com/cc421719-73a6-4d4d-9bf8-171e46c4e275">IFunctionInstance</a> interface pointer that receives the function instance.


## -returns



Possible return values include, but are not limited to, the following.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The function instance identified by <i>pInstanceIdentity</i> is not present in the function instance collection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>pdwIndex</i> or <i>pInstanceIdentity</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate the memory required to perform this operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8ac1a406-92f3-4e39-985e-ab8fa7d28751">IFunctionInstanceCollection</a>
 

 

