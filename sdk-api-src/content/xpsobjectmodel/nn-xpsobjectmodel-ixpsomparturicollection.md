---
UID: NN:xpsobjectmodel.IXpsOMPartUriCollection
title: IXpsOMPartUriCollection
author: windows-sdk-content
description: A collection of IOpcPartUri interface pointers.
old-location: xps\ixpsomparturicollection.htm
tech.root: printdocs
ms.assetid: 05fe9700-19e6-4e63-9693-cfa4b019f643
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsOMPartUriCollection, IXpsOMPartUriCollection interface [XPS Documents and Packaging], IXpsOMPartUriCollection interface [XPS Documents and Packaging],described, xps.ixpsomparturicollection, xpsobjectmodel/IXpsOMPartUriCollection
ms.prod: windows
ms.technology: windows-sdk
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
 - IXpsOMPartUriCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPartUriCollection interface


## -description


A collection of <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface pointers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMPartUriCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsOMPartUriCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMPartUriCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53d450cf-3e31-4d17-99cc-0552df771024">Append</a>
</td>
<td align="left" width="63%">
Appends an <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface to the end of the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d7fcc13-13f5-494d-b6b2-d1180902ec08">GetAt</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface pointer from a specified location in the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa716168-4584-4622-bfdf-7b022ff202c6">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface pointers in the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/672e3cc7-ac25-4d9d-9983-66cf6d26f574">InsertAt</a>
</td>
<td align="left" width="63%">
Inserts an <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface pointer at a specified location in the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db5e7595-eba0-454f-8fb3-f129ab537886">RemoveAt</a>
</td>
<td align="left" width="63%">
Removes and releases an <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface pointer from a specified location in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b41602ae-7d9e-48e4-b9f4-8db09e65f5c8">SetAt</a>
</td>
<td align="left" width="63%">
Replaces an <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface pointer at a specified location in the collection.
            

</td>
</tr>
</table> 


## -remarks



For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/0ed86fd1-ebc0-4eb6-a332-0dea3a21c100">IXpsOMObjectFactory::CreatePartUri</a>



<a href="https://msdn.microsoft.com/1127a314-43c8-43a2-a06e-88858a43c519">IXpsOMObjectFactory::CreatePartUriCollection</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

