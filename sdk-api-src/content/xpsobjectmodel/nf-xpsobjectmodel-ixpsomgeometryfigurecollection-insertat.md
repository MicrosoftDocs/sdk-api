---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigureCollection.InsertAt
title: IXpsOMGeometryFigureCollection::InsertAt
author: windows-sdk-content
description: Inserts an IXpsOMGeometryFigure interface pointer at a specified location in the collection.
old-location: xps\ixpsomgeometryfigurecollection_insertat.htm
tech.root: printdocs
ms.assetid: 1d550f36-ef0a-4a01-9c40-83e022634f73
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IXpsOMGeometryFigureCollection interface [XPS Documents and Packaging],InsertAt method, IXpsOMGeometryFigureCollection.InsertAt, IXpsOMGeometryFigureCollection::InsertAt, InsertAt, InsertAt method [XPS Documents and Packaging], InsertAt method [XPS Documents and Packaging],IXpsOMGeometryFigureCollection interface, xps.ixpsomgeometryfigurecollection_insertat, xpsobjectmodel/IXpsOMGeometryFigureCollection::InsertAt
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IXpsOMGeometryFigureCollection.InsertAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xpsobjectmodel.h
: 
- IXpsOMGeometryFigureCollection.InsertAt
: 
---

# IXpsOMGeometryFigureCollection::InsertAt


## -description


Inserts an <a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a> interface pointer at a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index in the collection where the interface pointer that is passed in <i>geometryFigure</i>  is to be inserted.


### -param geometryFigure [in]

The <a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a> interface pointer that is to be inserted at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



At the location specified by <i>index</i>, this method inserts the <a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a> interface pointer that is passed in <i>geometryFigure</i>.  Prior to the insertion, the pointer in this and all subsequent locations  is moved up by one index.

For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a>



<a href="https://msdn.microsoft.com/24ed79ff-9160-4e9b-b322-c538b30f113b">IXpsOMGeometryFigureCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

