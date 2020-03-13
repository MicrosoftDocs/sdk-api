---
UID: NF:xpsobjectmodel.IXpsOMDocumentCollection.InsertAt
title: IXpsOMDocumentCollection::InsertAt (xpsobjectmodel.h)
description: Inserts an IXpsOMDocument interface pointer at a specified location in the collection.
old-location: xps\ixpsomdocumentcollection_insertat.htm
tech.root: printdocs
ms.assetid: 2c968705-4fa5-4a74-8ae7-6bd4161f767f
ms.date: 12/05/2018
ms.keywords: IXpsOMDocumentCollection interface [XPS Documents and Packaging],InsertAt method, IXpsOMDocumentCollection.InsertAt, IXpsOMDocumentCollection::InsertAt, InsertAt, InsertAt method [XPS Documents and Packaging], InsertAt method [XPS Documents and Packaging],IXpsOMDocumentCollection interface, xps.ixpsomdocumentcollection_insertat, xpsobjectmodel/IXpsOMDocumentCollection::InsertAt
f1_keywords:
- xpsobjectmodel/IXpsOMDocumentCollection.InsertAt
dev_langs:
- c++
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
- IXpsOMDocumentCollection.InsertAt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMDocumentCollection::InsertAt


## -description


Inserts an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument">IXpsOMDocument</a> interface pointer at a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index of the collection where the interface pointer that is passed in  <i>document</i> is to be inserted.


### -param document [in]

The <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument">IXpsOMDocument</a> interface pointer that is to be inserted at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



At the location specified by <i>index</i>, this method inserts the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument">IXpsOMDocument</a> interface pointer that is passed in <i>document</i>.  Prior to the insertion, the pointer in this and all subsequent locations  is moved up by one index.

For more information about the collection methods, see  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument">IXpsOMDocument</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection">IXpsOMDocumentCollection</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372931(v=vs.85)">Working with XPS OM Collection Interfaces</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>
 

 

