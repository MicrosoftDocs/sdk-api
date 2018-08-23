---
UID: NF:comcat.IEnumCATEGORYINFO.Next
title: IEnumCATEGORYINFO::Next
author: windows-sdk-content
description: Retrieves the specified number of items in the enumeration sequence.
old-location: com\ienumcategoryinfo_next.htm
old-project: com
ms.assetid: d40816ca-b729-4251-b39b-a4c4ebec7118
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IEnumCATEGORYINFO interface [COM],Next method, IEnumCATEGORYINFO.Next, IEnumCATEGORYINFO::Next, Next, Next method [COM], Next method [COM],IEnumCATEGORYINFO interface, _com_ienumcategoryinfo_next, com.ienumcategoryinfo_next, comcat/IEnumCATEGORYINFO::Next
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comcat.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Comcat.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ServerInformation, *PServerInformation
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComCat.h
api_name:
 - IEnumCATEGORYINFO.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IEnumCATEGORYINFO::Next


## -description


Retrieves the specified number of items in the enumeration sequence.


## -parameters




### -param celt [in]

The number of items to be retrieved. If there are fewer than the requested number of items left in the sequence, this method retrieves the remaining elements.


### -param rgelt [out]

An array of enumerated items.

The enumerator is responsible for allocating any memory, and the caller is responsible for freeing it. If <i>celt</i> is greater than 1, the caller must also pass a non-NULL pointer passed to <i>pceltFetched</i> to know how many pointers to release.


### -param pceltFetched [out]

The number of items that were retrieved. This parameter is always less than or equal to the number of items requested.


## -returns



If the method retrieves the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.




## -see-also




<a href="https://msdn.microsoft.com/a5f0cb04-595d-4388-8943-79b9da76022b">CATEGORYINFO</a>



<a href="https://msdn.microsoft.com/87469ace-ae34-40e5-aab6-f26a4bc50b54">IEnumCATEGORYINFO</a>
 

 

