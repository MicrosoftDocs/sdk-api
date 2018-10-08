---
UID: NF:functiondiscoveryapi.IFunctionInstanceCollection.Remove
title: IFunctionInstanceCollection::Remove
author: windows-sdk-content
description: Deletes the specified function instance and returns a pointer to the function instance being removed.
old-location: ncd\ifunctioninstancecollection_remove.htm
tech.root: fundisc
ms.assetid: e5abe3e0-a07c-45e4-a590-133f6b30a7f7
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IFunctionInstanceCollection interface,Remove method, IFunctionInstanceCollection.Remove, IFunctionInstanceCollection::Remove, Remove, Remove method, Remove method,IFunctionInstanceCollection interface, functiondiscoveryapi/IFunctionInstanceCollection::Remove, ncd.ifunctioninstancecollection_remove
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
req.lib: 
req.dll: FunDisc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunDisc.dll
api_name:
 - IFunctionInstanceCollection.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFunctionInstanceCollection::Remove


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Deletes the specified function instance and returns a pointer to the function instance being removed.


## -parameters




### -param dwIndex [in]

The index number within the collection.


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
 

 

