---
UID: NF:pla.IValueMap.Add
title: IValueMap::Add
author: windows-sdk-content
description: Adds an item to the collection.
old-location: pla\ivaluemap_add.htm
old-project: PLA
ms.assetid: 4a6f074d-8d18-44ea-bbbc-8d3a7f6c033a
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: Add, Add method [PLA], Add method [PLA],IValueMap interface, IValueMap interface [PLA],Add method, IValueMap.Add, IValueMap::Add, base.ivaluemap_add, pla.ivaluemap_add, pla/IValueMap::Add
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FolderActionSteps
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IValueMap.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IValueMap::Add


## -description


Adds an item to the collection.


## -parameters




### -param value






#### - vValue [in]

An <b>IDispatch</b> interface of the <a href="https://msdn.microsoft.com/5fab2a62-d974-49f7-ac81-c704d9d8624c">IValueMapItem</a> interface to add to the collection. The variant type is VT_DISPATCH. 

You can also add a string or integer value. If the value is an integer (the variant type is VT_I4, VT_UI4, VT_I8, or VT_UI8), PLA adds an item with the specified value. 

If the value is a string  (the variant type is VT_BSTR), PLA tries to convert the string to an integer. If successful, PLA adds an item with the specified integer value. If PLA cannot convert the string, PLA searches the collection for a key that matches the string. If found, PLA enables the item; otherwise, the add fails.


## -returns



Returns S_OK if successful.




## -see-also




<a href="https://msdn.microsoft.com/a7134395-91c6-4ea1-8b76-63830048289f">IValueMap</a>



<a href="https://msdn.microsoft.com/80893a3d-fcfc-475f-86ad-d19bb9e43ee0">IValueMap::AddRange</a>



<a href="https://msdn.microsoft.com/dc674243-ec0f-496f-bffb-faf4262a42c7">IValueMap::Remove</a>
 

 

