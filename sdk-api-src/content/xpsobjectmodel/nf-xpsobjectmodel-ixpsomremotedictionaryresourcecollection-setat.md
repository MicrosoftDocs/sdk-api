---
UID: NF:xpsobjectmodel.IXpsOMRemoteDictionaryResourceCollection.SetAt
title: IXpsOMRemoteDictionaryResourceCollection::SetAt (xpsobjectmodel.h)
author: windows-sdk-content
description: Replaces an IXpsOMRemoteDictionaryResource interface pointer at a specified location in the collection.
old-location: xps\ixpsomremotedictionaryresourcecollection_setat.htm
tech.root: printdocs
ms.assetid: 45e33503-dff9-4c59-8d9a-883ff56a30f3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMRemoteDictionaryResourceCollection interface [XPS Documents and Packaging],SetAt method, IXpsOMRemoteDictionaryResourceCollection.SetAt, IXpsOMRemoteDictionaryResourceCollection::SetAt, SetAt, SetAt method [XPS Documents and Packaging], SetAt method [XPS Documents and Packaging],IXpsOMRemoteDictionaryResourceCollection interface, xps.ixpsomremotedictionaryresourcecollection_setat, xpsobjectmodel/IXpsOMRemoteDictionaryResourceCollection::SetAt
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
 - IXpsOMRemoteDictionaryResourceCollection.SetAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMRemoteDictionaryResourceCollection::SetAt


## -description


Replaces an <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface pointer at a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index in the collection where an <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface pointer is to be replaced.


### -param object [in]

The <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface pointer that will replace current contents at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



At the location specified by <i>index</i>, this method releases the <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface referenced by the existing pointer, then writes the pointer that is passed in <i>object</i>.

For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a>



<a href="https://msdn.microsoft.com/50c9bd7a-226f-4785-96b4-d0b5e861ae37">IXpsOMRemoteDictionaryResourceCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

