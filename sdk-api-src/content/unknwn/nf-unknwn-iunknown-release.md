---
UID: NF:unknwn.IUnknown.Release
title: IUnknown::Release method
author: windows-driver-content
description: Decrements the reference count for an interface on an object.
old-location: com\iunknown_release.htm
old-project: com
ms.assetid: 4b494c6f-f0ee-4c35-ae45-ed956f40dc7a
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IUnknown, IUnknown interface [COM], Release method, IUnknown::Release, Release method [COM], Release method [COM], IUnknown interface, Release,IUnknown.Release, _com_iunknown_release, com.iunknown_release, unknwnbase/IUnknown::Release
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: unknwn.h
req.include-header: Unknwn.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Unknwn.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	unknwnbase.h
api_name:
-	IUnknown.Release
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IUnknown::Release method


## -description


Decrements the reference count for an interface on an object.


## -parameters






## -returns



The method returns the new reference count. This value is intended to be used only for test purposes.




## -remarks



When the reference count on an object reaches zero, <b>Release</b> must cause the interface pointer to free itself. When the released pointer is the only existing reference to an object (whether the object supports single or multiple interfaces), the implementation must free the object.

Note that aggregation of objects restricts the ability to recover interface pointers.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Call this method when you no longer need to use an interface pointer. If you are writing a method that takes an in-out parameter, call <b>Release</b> on the pointer you are passing in before copying the out-value on top of it.




## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

