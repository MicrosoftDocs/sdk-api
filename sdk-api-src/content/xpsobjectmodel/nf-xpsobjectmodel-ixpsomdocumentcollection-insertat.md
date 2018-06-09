---
UID: NF:xpsobjectmodel.IXpsOMDocumentCollection.InsertAt
title: IXpsOMDocumentCollection::InsertAt
author: windows-sdk-content
description: Inserts an IXpsOMDocument interface pointer at a specified location in the collection.
old-location: xps\ixpsomdocumentcollection_insertat.htm
old-project: printdocs
ms.assetid: 2c968705-4fa5-4a74-8ae7-6bd4161f767f
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IXpsOMDocumentCollection interface [XPS Documents and Packaging],InsertAt method, IXpsOMDocumentCollection.InsertAt, IXpsOMDocumentCollection::InsertAt, InsertAt, InsertAt method [XPS Documents and Packaging], InsertAt method [XPS Documents and Packaging],IXpsOMDocumentCollection interface, xps.ixpsomdocumentcollection_insertat, xpsobjectmodel/IXpsOMDocumentCollection::InsertAt
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMDocumentCollection.InsertAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMDocumentCollection::InsertAt


## -description


Inserts an <a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a> interface pointer at a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index of the collection where the interface pointer that is passed in  <i>document</i> is to be inserted.


### -param document [in]

The <a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a> interface pointer that is to be inserted at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



At the location specified by <i>index</i>, this method inserts the <a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a> interface pointer that is passed in <i>document</i>.  Prior to the insertion, the pointer in this and all subsequent locations  is moved up by one index.

For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a>



<a href="https://msdn.microsoft.com/4f3acae9-10a0-47ff-9170-a40abe230580">IXpsOMDocumentCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

