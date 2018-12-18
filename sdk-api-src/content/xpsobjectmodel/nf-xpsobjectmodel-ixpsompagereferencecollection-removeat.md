---
UID: NF:xpsobjectmodel.IXpsOMPageReferenceCollection.RemoveAt
title: IXpsOMPageReferenceCollection::RemoveAt
author: windows-sdk-content
description: Removes and releases an IXpsOMPageReference interface pointer from a specified location in the collection.
old-location: xps\ixpsompagereferencecollection_removeat.htm
tech.root: printdocs
ms.assetid: 905ed1ea-b694-4620-8a71-2f0bfb831af4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXpsOMPageReferenceCollection interface [XPS Documents and Packaging],RemoveAt method, IXpsOMPageReferenceCollection.RemoveAt, IXpsOMPageReferenceCollection::RemoveAt, RemoveAt, RemoveAt method [XPS Documents and Packaging], RemoveAt method [XPS Documents and Packaging],IXpsOMPageReferenceCollection interface, xps.ixpsompagereferencecollection_removeat, xpsobjectmodel/IXpsOMPageReferenceCollection::RemoveAt
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
 - IXpsOMPageReferenceCollection.RemoveAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPageReferenceCollection::RemoveAt


## -description


Removes and releases an <a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a> interface pointer from a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index in the collection from which  an <a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a> interface pointer is to be removed and released.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This method releases the interface  referenced by the pointer at  the location specified by <i>index</i>. After releasing the interface, this method compacts the collection by   reducing by 1 the index of each pointer subsequent to <i>index</i>.

For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a>



<a href="https://msdn.microsoft.com/4b51bc29-c653-41fa-bbd3-9ff529f84e4e">IXpsOMPageReferenceCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

