---
UID: NF:xpsobjectmodel.IXpsOMDashCollection.RemoveAt
title: IXpsOMDashCollection::RemoveAt method
author: windows-driver-content
description: Removes and frees an XPS_DASH structure from a specified location in the collection.
old-location: xps\ixpsomdashcollection_removeat.htm
old-project: printdocs
ms.assetid: 5ccce0d4-c764-4da4-9d7c-463921a92a6a
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsOMDashCollection, IXpsOMDashCollection interface [XPS Documents and Packaging], RemoveAt method, IXpsOMDashCollection::RemoveAt, RemoveAt method [XPS Documents and Packaging], RemoveAt method [XPS Documents and Packaging], IXpsOMDashCollection interface, RemoveAt,IXpsOMDashCollection.RemoveAt, xps.ixpsomdashcollection_removeat, xpsobjectmodel/IXpsOMDashCollection::RemoveAt
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
-	IXpsOMDashCollection.RemoveAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMDashCollection::RemoveAt method


## -description


Removes and frees an <a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a> structure from a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index in the collection from which  an <a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a> structure is to be removed and freed.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This method removes and frees  the <a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a> structure  referenced by the pointer at  the location specified by <i>index</i>. After freeing the structure, this method compacts the collection by   reducing by 1 the index of each pointer subsequent to <i>index</i>.

The figure that follows illustrates how the collection is changed by the <b>RemoveAt</b> method.

<img alt="A figure that shows how RemoveAt removes an entry from the dash collection" src="../images/dashcollection_removeat.png"/>



## -see-also




<a href="https://msdn.microsoft.com/02a152a1-e117-42fb-8428-a2b28e6540a9">IXpsOMDashCollection</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a>
 

 

