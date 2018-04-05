---
UID: NF:functiondiscoveryapi.IFunctionInstanceCollection.Delete
title: IFunctionInstanceCollection::Delete method
author: windows-driver-content
description: Removes the specified function instance from the collection.
old-location: ncd\ifunctioninstancecollection_delete.htm
old-project: FunDisc
ms.assetid: e7f94912-9656-4a6b-8754-eb37358b5f9d
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Delete method, Delete method, IFunctionInstanceCollection interface, Delete,IFunctionInstanceCollection.Delete, IFunctionInstanceCollection, IFunctionInstanceCollection interface, Delete method, IFunctionInstanceCollection::Delete, functiondiscoveryapi/IFunctionInstanceCollection::Delete, ncd.ifunctioninstancecollection_delete
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
-	IFunctionInstanceCollection.Delete
product: Windows
targetos: Windows
req.lib: 
req.dll: FunDisc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFunctionInstanceCollection::Delete method


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Removes the specified function instance from the collection.


## -parameters




### -param dwIndex [in]

The index number of the item to be removed from the collection.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>dwIndex</i> is invalid.

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
 

 

