---
UID: NF:unknwnbase.IUnknown.AddRef
title: IUnknown::AddRef
author: windows-sdk-content
description: Increments the reference count for an interface on an object. This method should be called for every new copy of a pointer to an interface on an object.
old-location: com\iunknown_addref.htm
old-project: com
ms.assetid: b4316efd-73d4-4995-b898-8025a316ba63
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: AddRef, AddRef method [COM], AddRef method [COM],IUnknown interface, IUnknown interface [COM],AddRef method, IUnknown.AddRef, IUnknown::AddRef, _com_iunknown_addref, com.iunknown_addref, unknwnbase/IUnknown::AddRef
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: unknwnbase.h
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
tech.root: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - unknwnbase.h
api_name:
 - IUnknown.AddRef
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IUnknown::AddRef


## -description


Increments the reference count for an interface on an object. This method should be called for every new copy of a pointer to an interface on an object.


## -parameters






## -returns



The method returns the new reference count. This value is intended to be used only for test purposes.




## -remarks



Objects use a reference counting mechanism to ensure that the lifetime of the object includes the lifetime of references to it. You use <b>AddRef</b> to stabilize a copy of an interface pointer. It can also be called when the life of a cloned pointer must extend beyond the lifetime of the original pointer. The cloned pointer must be released by calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a>.

The internal reference counter that <b>AddRef</b> maintains should be a 32-bit unsigned integer.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Call this method for every new copy of an interface pointer that you make. For example, if you are passing a copy of a pointer back from a method, you must call <b>AddRef</b> on that pointer. You must also call <b>AddRef</b> on a pointer before passing it as an in-out parameter to a method; the method will call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> before copying the out-value on top of it.




## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

