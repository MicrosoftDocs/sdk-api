---
UID: NF:xpsobjectmodel.IXpsOMDashCollection.SetAt
title: IXpsOMDashCollection::SetAt
author: windows-sdk-content
description: Replaces an XPS_DASH structure at a specified location in the collection.
old-location: xps\ixpsomdashcollection_setat.htm
old-project: printdocs
ms.assetid: c0ea0ae0-2c28-4478-82fc-3e80bc70eef8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsOMDashCollection interface [XPS Documents and Packaging],SetAt method, IXpsOMDashCollection.SetAt, IXpsOMDashCollection::SetAt, SetAt, SetAt method [XPS Documents and Packaging], SetAt method [XPS Documents and Packaging],IXpsOMDashCollection interface, xps.ixpsomdashcollection_setat, xpsobjectmodel/IXpsOMDashCollection::SetAt
ms.prod: windows
ms.technology: windows-sdk
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
 - IXpsOMDashCollection.SetAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMDashCollection::SetAt


## -description


Replaces an <a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a> structure at a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index in the collection where an <a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a> structure is to be replaced.


### -param dash [in]

A pointer to the <a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a> structure that will replace the current contents at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



At the location specified by <i>index</i>, this method frees the existing <a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a> structure then replaces it with the structure that is passed in <i>dash</i>.

The figure that follows illustrates how the collection is changed by the <b>SetAt</b> method.

<img alt="A figure that shows how SetAt changes an entry in the dash collection" src="../images/dashcollection_setat.png"/>



## -see-also




<a href="https://msdn.microsoft.com/02a152a1-e117-42fb-8428-a2b28e6540a9">IXpsOMDashCollection</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a>
 

 

