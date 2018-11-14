---
UID: NN:xpsobjectmodel.IXpsOMGeometryFigureCollection
title: IXpsOMGeometryFigureCollection
author: windows-sdk-content
description: A collection of IXpsOMGeometryFigure interface pointers.
old-location: xps\ixpsomgeometryfigurecollection.htm
tech.root: printdocs
ms.assetid: 24ed79ff-9160-4e9b-b322-c538b30f113b
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IXpsOMGeometryFigureCollection, IXpsOMGeometryFigureCollection interface [XPS Documents and Packaging], IXpsOMGeometryFigureCollection interface [XPS Documents and Packaging],described, xps.ixpsomgeometryfigurecollection, xpsobjectmodel/IXpsOMGeometryFigureCollection
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
 - IXpsOMGeometryFigureCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMGeometryFigureCollection interface


## -description


A collection of <a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a> interface pointers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMGeometryFigureCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsOMGeometryFigureCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMGeometryFigureCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9481cd02-74f8-42f6-a347-454dae2aa579">Append</a>
</td>
<td align="left" width="63%">
Appends an <a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a> interface to the end of the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/adf36d84-7bfd-4a8c-b6e7-5a8622245ae5">GetAt</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a> interface pointer from a specified location in the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/119e36b6-08c4-4578-9f93-cedeac14b2cc">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of <a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a> interface pointers in the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d550f36-ef0a-4a01-9c40-83e022634f73">InsertAt</a>
</td>
<td align="left" width="63%">
Inserts an <a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a> interface pointer at a specified location in the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3030eea-e87f-4bb8-9835-e6bc052ff0ef">RemoveAt</a>
</td>
<td align="left" width="63%">
Removes and releases an <a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a> interface pointer from a specified location in the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59612109-8500-4bd9-a37c-120ef12aded4">SetAt</a>
</td>
<td align="left" width="63%">
Replaces an <a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a> interface pointer at a specified location in the collection.
            

</td>
</tr>
</table> 


## -remarks



For more information about the collection methods, see <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

