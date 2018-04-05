---
UID: NF:xpsobjectmodel.IXpsOMRemoteDictionaryResourceCollection.RemoveAt
title: IXpsOMRemoteDictionaryResourceCollection::RemoveAt method
author: windows-driver-content
description: Removes and releases an IXpsOMRemoteDictionaryResource interface pointer from a specified location in the collection.
old-location: xps\ixpsomremotedictionaryresourcecollection_removeat.htm
old-project: printdocs
ms.assetid: a144a3b4-3935-4377-b97d-3d3a723ea3b7
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsOMRemoteDictionaryResourceCollection, IXpsOMRemoteDictionaryResourceCollection interface [XPS Documents and Packaging], RemoveAt method, IXpsOMRemoteDictionaryResourceCollection::RemoveAt, RemoveAt method [XPS Documents and Packaging], RemoveAt method [XPS Documents and Packaging], IXpsOMRemoteDictionaryResourceCollection interface, RemoveAt,IXpsOMRemoteDictionaryResourceCollection.RemoveAt, xps.ixpsomremotedictionaryresourcecollection_removeat, xpsobjectmodel/IXpsOMRemoteDictionaryResourceCollection::RemoveAt
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
-	IXpsOMRemoteDictionaryResourceCollection.RemoveAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMRemoteDictionaryResourceCollection::RemoveAt method


## -description


Removes and releases an <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface pointer from a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index in the collection from which  an <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface pointer is to be removed and released.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This method releases the interface  referenced by the pointer at  the location specified by <i>index</i>. After releasing the interface, this method compacts the collection by   reducing by 1 the index of each pointer subsequent to <i>index</i>.

For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a>



<a href="https://msdn.microsoft.com/50c9bd7a-226f-4785-96b4-d0b5e861ae37">IXpsOMRemoteDictionaryResourceCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

