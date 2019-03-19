---
UID: NF:xpsobjectmodel.IXpsOMSignatureBlockResourceCollection.InsertAt
title: IXpsOMSignatureBlockResourceCollection::InsertAt (xpsobjectmodel.h)
author: windows-sdk-content
description: Inserts an IXpsOMSignatureBlockResource interface pointer at a specified location in the collection.
old-location: xps\ixpsomsignatureblockresourcecollection_insertat.htm
tech.root: printdocs
ms.assetid: bcb9d712-35b6-4dfc-91dc-dd376950e1e8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXpsOMSignatureBlockResourceCollection interface [XPS Documents and Packaging],InsertAt method, IXpsOMSignatureBlockResourceCollection.InsertAt, IXpsOMSignatureBlockResourceCollection::InsertAt, InsertAt, InsertAt method [XPS Documents and Packaging], InsertAt method [XPS Documents and Packaging],IXpsOMSignatureBlockResourceCollection interface, xps.ixpsomsignatureblockresourcecollection_insertat, xpsobjectmodel/IXpsOMSignatureBlockResourceCollection::InsertAt
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
 - IXpsOMSignatureBlockResourceCollection.InsertAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMSignatureBlockResourceCollection::InsertAt


## -description


Inserts an <a href="https://msdn.microsoft.com/f5052470-487d-4f47-8d42-70538a4a45a8">IXpsOMSignatureBlockResource</a> interface pointer at a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index in the collection where the interface pointer that is passed in <i>signatureBlockResource</i>  is to be inserted.


### -param signatureBlockResource [in]

The <a href="https://msdn.microsoft.com/f5052470-487d-4f47-8d42-70538a4a45a8">IXpsOMSignatureBlockResource</a> interface pointer that is to be inserted at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



At the location specified by <i>index</i>, this method inserts the <a href="https://msdn.microsoft.com/f5052470-487d-4f47-8d42-70538a4a45a8">IXpsOMSignatureBlockResource</a> interface pointer that is passed in <i>signatureBlockResource</i>.  Prior to the insertion, the pointer in this and all subsequent locations  is moved up by one index.

For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/f5052470-487d-4f47-8d42-70538a4a45a8">IXpsOMSignatureBlockResource</a>



<a href="https://msdn.microsoft.com/681bdb9c-69dd-4bf6-a4b3-c490f7a0363e">IXpsOMSignatureBlockResourceCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

