---
UID: NF:pla.IValueMap.Remove
title: IValueMap::Remove method
author: windows-driver-content
description: Removes an item from the collection.
old-location: pla\ivaluemap_remove.htm
old-project: PLA
ms.assetid: dc674243-ec0f-496f-bffb-faf4262a42c7
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IValueMap, IValueMap interface [PLA], Remove method, IValueMap::Remove, Remove method [PLA], Remove method [PLA], IValueMap interface, Remove,IValueMap.Remove, base.ivaluemap_remove, pla.ivaluemap_remove, pla/IValueMap::Remove
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FolderActionSteps
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Pla.dll
api_name:
-	IValueMap.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IValueMap::Remove method


## -description


Removes an item from the collection.


## -parameters




### -param value






#### - vValue [in]

The zero-based index of the item to remove from the collection. The variant type can be VT_I4, VT_UI4, or VT_DISPATCH.


## -returns



Returns S_OK if successful.




## -remarks



If the variant type is VT_DISPATCH, pass the <b>IDispatch</b> interface of the <a href="https://msdn.microsoft.com/5fab2a62-d974-49f7-ac81-c704d9d8624c">IValueMapItem</a> interface to be removed.




## -see-also




<a href="https://msdn.microsoft.com/a7134395-91c6-4ea1-8b76-63830048289f">IValueMap</a>



<a href="https://msdn.microsoft.com/4a6f074d-8d18-44ea-bbbc-8d3a7f6c033a">IValueMap::Add</a>



<a href="https://msdn.microsoft.com/41c80954-efc2-47ff-87e2-f33d7123cb40">IValueMap::Clear</a>
 

 

