---
UID: NF:xpsobjectmodel.IXpsOMGradientStopCollection.InsertAt
title: IXpsOMGradientStopCollection::InsertAt (xpsobjectmodel.h)
author: windows-sdk-content
description: Inserts an IXpsOMGradientStop interface pointer at a specified location in the collection.
old-location: xps\ixpsomgradientstopcollection_insertat.htm
tech.root: printdocs
ms.assetid: b5ab5db8-ad94-4949-9d74-bddef3f29895
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMGradientStopCollection interface [XPS Documents and Packaging],InsertAt method, IXpsOMGradientStopCollection.InsertAt, IXpsOMGradientStopCollection::InsertAt, InsertAt, InsertAt method [XPS Documents and Packaging], InsertAt method [XPS Documents and Packaging],IXpsOMGradientStopCollection interface, xps.ixpsomgradientstopcollection_insertat, xpsobjectmodel/IXpsOMGradientStopCollection::InsertAt
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
 - IXpsOMGradientStopCollection.InsertAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMGradientStopCollection::InsertAt


## -description


Inserts an <a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a> interface pointer at a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index in the collection where the interface pointer that is passed in <i>stop</i>  is to be inserted.


### -param stop [in]

The <a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a> interface pointer to be inserted at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



At the location specified by <i>index</i>, this method inserts the <a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a> interface pointer that is passed in <i>stop</i>.  Prior to the insertion, the pointer in this and all subsequent locations  is moved up by one index.

For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a>



<a href="https://msdn.microsoft.com/1f51f818-e9bb-4d88-9795-4e6890d24b8c">IXpsOMGradientStopCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

