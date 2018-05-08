---
UID: NF:xpsobjectmodel.IXpsOMImageResourceCollection.InsertAt
title: IXpsOMImageResourceCollection::InsertAt
author: windows-driver-content
description: Inserts an IXpsOMImageResource interface pointer at a specified location in the collection.
old-location: xps\ixpsomimageresourcecollection_insertat.htm
old-project: printdocs
ms.assetid: 46bb3a49-f875-4b52-98f4-cec475f46019
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsOMImageResourceCollection interface [XPS Documents and Packaging],InsertAt method, IXpsOMImageResourceCollection.InsertAt, IXpsOMImageResourceCollection::InsertAt, InsertAt, InsertAt method [XPS Documents and Packaging], InsertAt method [XPS Documents and Packaging],IXpsOMImageResourceCollection interface, xps.ixpsomimageresourcecollection_insertat, xpsobjectmodel/IXpsOMImageResourceCollection::InsertAt
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
-	IXpsOMImageResourceCollection.InsertAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMImageResourceCollection::InsertAt


## -description


Inserts an <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface pointer at a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index in the collection where the interface pointer that is passed in <i>object</i>  is to be inserted.


### -param object [in]

The <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface pointer that will be inserted at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



At the location specified by <i>index</i>, this method inserts the <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface pointer that is passed in <i>object</i>.  Prior to the insertion, the pointer in this and all subsequent locations  is moved up by one index.

For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a>



<a href="https://msdn.microsoft.com/aed8b23e-71fd-49e6-aae9-006a59e0111b">IXpsOMImageResourceCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

