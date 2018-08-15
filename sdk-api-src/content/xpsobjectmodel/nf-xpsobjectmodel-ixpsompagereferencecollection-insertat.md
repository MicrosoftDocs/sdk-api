---
UID: NF:xpsobjectmodel.IXpsOMPageReferenceCollection.InsertAt
title: IXpsOMPageReferenceCollection::InsertAt
author: windows-sdk-content
description: Inserts an IXpsOMPageReference interface pointer at a specified location in the collection.
old-location: xps\ixpsompagereferencecollection_insertat.htm
old-project: printdocs
ms.assetid: 829d0b81-90e2-4051-a9a7-7f71602f8c13
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsOMPageReferenceCollection interface [XPS Documents and Packaging],InsertAt method, IXpsOMPageReferenceCollection.InsertAt, IXpsOMPageReferenceCollection::InsertAt, InsertAt, InsertAt method [XPS Documents and Packaging], InsertAt method [XPS Documents and Packaging],IXpsOMPageReferenceCollection interface, xps.ixpsompagereferencecollection_insertat, xpsobjectmodel/IXpsOMPageReferenceCollection::InsertAt
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.redist: 
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
 - IXpsOMPageReferenceCollection.InsertAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPageReferenceCollection::InsertAt


## -description


Inserts an <a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a> interface pointer at a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index in the collection where the interface pointer that is passed in <i>pageReference</i> is to be inserted.


### -param pageReference [in]

The <a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a> interface pointer that is to be inserted at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



At the location specified by <i>index</i>, this method inserts the <a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a> interface pointer that is passed in <i>pageReference</i>.  Prior to the insertion, the pointer in this and all subsequent locations  is moved up by one index.

For more information about the collection methods, see <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a>



<a href="https://msdn.microsoft.com/4b51bc29-c653-41fa-bbd3-9ff529f84e4e">IXpsOMPageReferenceCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

