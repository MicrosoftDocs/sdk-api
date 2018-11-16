---
UID: NF:xpsobjectmodel.IXpsOMPageReferenceCollection.SetAt
title: IXpsOMPageReferenceCollection::SetAt
author: windows-sdk-content
description: Replaces an IXpsOMPageReference interface pointer at a specified location in the collection.
old-location: xps\ixpsompagereferencecollection_setat.htm
tech.root: printdocs
ms.assetid: b06b7ae2-e684-46a3-ab46-9f33cc6c10fc
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IXpsOMPageReferenceCollection interface [XPS Documents and Packaging],SetAt method, IXpsOMPageReferenceCollection.SetAt, IXpsOMPageReferenceCollection::SetAt, SetAt, SetAt method [XPS Documents and Packaging], SetAt method [XPS Documents and Packaging],IXpsOMPageReferenceCollection interface, xps.ixpsompagereferencecollection_setat, xpsobjectmodel/IXpsOMPageReferenceCollection::SetAt
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IXpsOMPageReferenceCollection.SetAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xpsobjectmodel.h
: 
- IXpsOMPageReferenceCollection.SetAt
: 
---

# IXpsOMPageReferenceCollection::SetAt


## -description


Replaces an <a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a> interface pointer at a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index in the collection where an <a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a> interface pointer is to be replaced.


### -param pageReference [in]

The <a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a> interface pointer that will replace current contents at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



At the location specified by <i>index</i>, this method releases the <a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a> interface referenced by the existing pointer, then writes the pointer that is passed in <i>pageReference</i>.

For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a>



<a href="https://msdn.microsoft.com/4b51bc29-c653-41fa-bbd3-9ff529f84e4e">IXpsOMPageReferenceCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

