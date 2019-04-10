---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigureCollection.GetAt
title: IXpsOMGeometryFigureCollection::GetAt (xpsobjectmodel.h)
author: windows-sdk-content
description: Gets an IXpsOMGeometryFigure interface pointer from a specified location in the collection.
old-location: xps\ixpsomgeometryfigurecollection_getat.htm
tech.root: printdocs
ms.assetid: adf36d84-7bfd-4a8c-b6e7-5a8622245ae5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAt, GetAt method [XPS Documents and Packaging], GetAt method [XPS Documents and Packaging],IXpsOMGeometryFigureCollection interface, IXpsOMGeometryFigureCollection interface [XPS Documents and Packaging],GetAt method, IXpsOMGeometryFigureCollection.GetAt, IXpsOMGeometryFigureCollection::GetAt, xps.ixpsomgeometryfigurecollection_getat, xpsobjectmodel/IXpsOMGeometryFigureCollection::GetAt
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
 - IXpsOMGeometryFigureCollection.GetAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMGeometryFigureCollection::GetAt


## -description


Gets an <a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a> interface pointer from a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index of the <a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a> interface pointer to be obtained.


### -param geometryFigure [out, retval]

The <a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a> interface pointer at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a>



<a href="https://msdn.microsoft.com/24ed79ff-9160-4e9b-b322-c538b30f113b">IXpsOMGeometryFigureCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

