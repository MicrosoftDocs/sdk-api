---
UID: NF:functiondiscoveryapi.IFunctionInstanceCollection.GetCount
title: IFunctionInstanceCollection::GetCount (functiondiscoveryapi.h)
author: windows-sdk-content
description: Gets the number of function instances in the collection.
old-location: ncd\ifunctioninstancecollection_getcount_method.htm
tech.root: FunDisc
ms.assetid: d74d10b1-dab1-4f7e-8dbc-434570bf9c79
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCount, GetCount method, GetCount method,IFunctionInstanceCollection interface, IFunctionInstanceCollection interface,GetCount method, IFunctionInstanceCollection.GetCount, IFunctionInstanceCollection::GetCount, functiondiscoveryapi/IFunctionInstanceCollection::GetCount, ncd.ifunctioninstancecollection_getcount_method
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
 - IFunctionInstanceCollection.GetCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFunctionInstanceCollection::GetCount


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the number of function instances in the collection.


## -parameters




### -param pdwCount [out]

The number of function instances.


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
The <i>pdwCount</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The <b>GetCount</b> and <a href="https://msdn.microsoft.com/b79b7cb2-c02a-4474-bd48-8907ebb118fa">Item</a> methods enables you to enumerate all of the function instances contained in a collection using a simple <b>for</b> or <b>while</b> loop.




## -see-also




<a href="https://msdn.microsoft.com/8ac1a406-92f3-4e39-985e-ab8fa7d28751">IFunctionInstanceCollection</a>
 

 

