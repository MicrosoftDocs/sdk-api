---
UID: NN:tapi3if.ITCollection
title: ITCollection
author: windows-sdk-content
description: The ITCollection interface allows Automation client applications, such as those written in Visual Basic, to retrieve collection information.
old-location: tapi3\itcollection.htm
tech.root: tapi
ms.assetid: 2286678a-68b9-4f4a-b36b-7fdf8cdad6a6
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITCollection, ITCollection interface [TAPI 2.2], ITCollection interface [TAPI 2.2],described, _tapi3_itcollection, tapi3.itcollection, tapi3if/ITCollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ITCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCollection interface


## -description


The 
<b>ITCollection</b> interface allows Automation client applications, such as those written in Visual Basic, to retrieve collection information. C or C++ programs use enumerator interfaces to retrieve the same information. Collection methods return a <b>VARIANT</b> which contains a pointer to an 
<b>ITCollection</b> interface.

The 
<a href="https://msdn.microsoft.com/d65f06c9-fecd-4ce6-af82-81acb48268e5">ITCollection2</a> interface is an extension of the 
<b>ITCollection</b> interface. 
<b>ITCollection2</b> exposes additional methods for modifying the collection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITCollection</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b84298f-f114-4171-a2ad-d14122cb4bc8">get__NewEnum</a>
</td>
<td align="left" width="63%">
Gets an enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/253c09db-4b64-43d0-8040-b3a2ab95af30">get_Count</a>
</td>
<td align="left" width="63%">
Gets the number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4e6de7e-99c4-415f-b3b4-7e8bf1f082fc">get_Item</a>
</td>
<td align="left" width="63%">
Given an index, returns an item in the collection.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/d65f06c9-fecd-4ce6-af82-81acb48268e5">ITCollection2</a>
 

 

