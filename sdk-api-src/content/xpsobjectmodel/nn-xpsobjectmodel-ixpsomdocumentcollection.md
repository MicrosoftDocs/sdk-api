---
UID: NN:xpsobjectmodel.IXpsOMDocumentCollection
title: IXpsOMDocumentCollection
author: windows-sdk-content
description: A collection of IXpsOMDocument interface pointers.
old-location: xps\ixpsomdocumentcollection.htm
tech.root: printdocs
ms.assetid: 4f3acae9-10a0-47ff-9170-a40abe230580
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IXpsOMDocumentCollection, IXpsOMDocumentCollection interface [XPS Documents and Packaging], IXpsOMDocumentCollection interface [XPS Documents and Packaging],described, xps.ixpsomdocumentcollection, xpsobjectmodel/IXpsOMDocumentCollection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMDocumentCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMDocumentCollection interface


## -description


A collection of <a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a> interface pointers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMDocumentCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsOMDocumentCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMDocumentCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ac969fd-72ad-4d4f-b2bb-25e0f4401179">Append</a>
</td>
<td align="left" width="63%">
Appends an <a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a> interface to the end of the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74649245-b6ec-4ebb-aa9b-8de9c0c6c761">GetAt</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a> interface pointer from a specified location in the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92ca1a4f-7fc8-4dd5-b594-6097e0ab2203">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of <a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a> interface pointers in the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c968705-4fa5-4a74-8ae7-6bd4161f767f">InsertAt</a>
</td>
<td align="left" width="63%">
Inserts an <a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a> interface pointer at a specified location in the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5e7d04c-c1da-4af7-9048-1a9b79ba4872">RemoveAt</a>
</td>
<td align="left" width="63%">
Removes and releases an <a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a> interface pointer from a specified location in the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71279337-33ec-4ed3-8c87-9c9b6844d26b">SetAt</a>
</td>
<td align="left" width="63%">
Replaces an <a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a> interface pointer at a specified location in the collection.
            

</td>
</tr>
</table> 


## -remarks



For more information about the collection methods, see <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

