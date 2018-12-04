---
UID: NF:functiondiscoveryapi.IFunctionInstanceCollection.Item
title: IFunctionInstanceCollection::Item
author: windows-sdk-content
description: Gets the specified function instance, by index.
old-location: ncd\ifunctioninstancecollection_item_method.htm
tech.root: fundisc
ms.assetid: b79b7cb2-c02a-4474-bd48-8907ebb118fa
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IFunctionInstanceCollection interface,Item method, IFunctionInstanceCollection.Item, IFunctionInstanceCollection::Item, Item, Item method, Item method,IFunctionInstanceCollection interface, functiondiscoveryapi/IFunctionInstanceCollection::Item, ncd.ifunctioninstancecollection_item_method
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
 - IFunctionInstanceCollection.Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFunctionInstanceCollection::Item


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the specified function instance, by index.


## -parameters




### -param dwIndex [in]

The zero-based index of the function instance to be retrieved.


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
The <i>ppFunctionInstance</i> parameter is <b>NULL</b> or <i>dwIndex</i> is out of range.

</td>
</tr>
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/d74d10b1-dab1-4f7e-8dbc-434570bf9c79">GetCount</a> and <b>Item</b> methods enables you to enumerate all of the function instances contained in a collection using a simple <b>for</b> or <b>while</b> loop.




## -see-also




<a href="https://msdn.microsoft.com/8ac1a406-92f3-4e39-985e-ab8fa7d28751">IFunctionInstanceCollection</a>
 

 

