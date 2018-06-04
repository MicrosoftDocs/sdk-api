---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# __MIDL_ICallFrame_0003 enumeration


## -description


Determines whether the copied call frame data can be shared with data in the parent frame by determining its lifetime dependency on the parent frame. 


## -enum-fields




### -field CALLFRAME_COPY_NESTED

The client will be responsible for using the copied call frame in a manner that its lifetime is nested in the lifetime of its parent frame making the data sharable. When this flag is used, very significant optimizations can be made and memory allocations avoided by cleverly sharing actual parameter data.

Only the interface pointers transitively reachable in the source frames are guaranteed to be deep copied and thus in the copy be stored in memory separate from that in which they are stored in the source frames; other data types may actually in the copied frame share memory with the source if the copy operation is intelligent enough to do so.


### -field CALLFRAME_COPY_INDEPENDENT

The copied call frame will have a lifetime independent from its parent.


## -remarks



A consequence is that whichever of these <b>CALLFRAME_COPY</b> flags are passed to <a href="https://msdn.microsoft.com/bf2d2e55-d9d1-48d6-817c-382c739d1acd">ICallFrame::Copy</a>, the interface pointers can be modified without consequence of disturbing the interface pointers residing in the parent frame.





## -see-also




<a href="https://msdn.microsoft.com/bf2d2e55-d9d1-48d6-817c-382c739d1acd">ICallFrame::Copy</a>
 

 

