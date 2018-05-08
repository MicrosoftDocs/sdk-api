---
UID: NF:xpsobjectmodel.IXpsOMRemoteDictionaryResourceCollection.InsertAt
title: IXpsOMRemoteDictionaryResourceCollection::InsertAt
author: windows-driver-content
description: Inserts an IXpsOMRemoteDictionaryResource interface pointer at a specified location in the collection.
old-location: xps\ixpsomremotedictionaryresourcecollection_insertat.htm
old-project: printdocs
ms.assetid: 22abb514-6574-4d7e-8ea5-2b0956b4e8a4
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsOMRemoteDictionaryResourceCollection interface [XPS Documents and Packaging],InsertAt method, IXpsOMRemoteDictionaryResourceCollection.InsertAt, IXpsOMRemoteDictionaryResourceCollection::InsertAt, InsertAt, InsertAt method [XPS Documents and Packaging], InsertAt method [XPS Documents and Packaging],IXpsOMRemoteDictionaryResourceCollection interface, xps.ixpsomremotedictionaryresourcecollection_insertat, xpsobjectmodel/IXpsOMRemoteDictionaryResourceCollection::InsertAt
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMRemoteDictionaryResourceCollection.InsertAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMRemoteDictionaryResourceCollection::InsertAt


## -description


Inserts an <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface pointer at a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index in the collection where the interface pointer that is passed in <i>object</i> is to be inserted.


### -param object [in]

The <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface pointer that is to be inserted at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



At the location specified by <i>index</i>, this method inserts the <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface pointer that is passed in <i>object</i>.  Prior to the insertion, the pointer in this and all subsequent locations  is moved up by one index.

For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a>



<a href="https://msdn.microsoft.com/50c9bd7a-226f-4785-96b4-d0b5e861ae37">IXpsOMRemoteDictionaryResourceCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

