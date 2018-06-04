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

# tagCOINIT enumeration


## -description


Determines the concurrency model used for incoming calls to objects created by this thread. This concurrency model can be either apartment-threaded or multithreaded.



## -enum-fields




### -field COINIT_APARTMENTTHREADED

Initializes the thread for apartment-threaded object concurrency (see Remarks).


### -field COINIT_MULTITHREADED

Initializes the thread for multithreaded object concurrency (see Remarks).


### -field COINIT_DISABLE_OLE1DDE

Disables DDE for OLE1 support.


### -field COINIT_SPEED_OVER_MEMORY

Increase memory usage in an attempt to increase performance.


## -remarks



When a thread is initialized through a call to <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>, you choose whether to initialize it as apartment-threaded or multithreaded by designating one of the members of <b>COINIT</b> as its second parameter. This designates how incoming calls to any object created by that thread are handled, that is, the object's concurrency.

Apartment-threading, while allowing for multiple threads of execution, serializes all incoming calls by requiring that calls to methods of objects created by this thread always run on the same thread â€“ the apartment/thread that created them. In addition, calls can arrive only at message-queue boundaries. Because of this serialization, it is not typically necessary to write concurrency control into the code for the object, other than to avoid calls to <a href="_win32_PeekMessage_cpp">PeekMessage</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/jj151552">SendMessage</a> during processing that must not be interrupted by other method invocations or calls to other objects in the same apartment/thread.



Multi-threading (also called free-threading) allows calls to methods of objects created by this thread to be run on any thread. There is no serialization of calls â€“ many calls may occur to the same method or to the same object or simultaneously. Multi-threaded object concurrency offers the highest performance and takes the best advantage of multiprocessor hardware for cross-thread, cross-process, and cross-machine calling, since calls to objects are not serialized in any way. This means, however, that the code for objects must enforce its own concurrency model, typically through the use of synchronization primitives, such as critical sections, semaphores, or mutexes. In addition, because the object doesn't control the lifetime of the threads that are accessing it, no thread-specific state may be stored in the object (in <a href="https://msdn.microsoft.com/40df7410-64d6-4edd-8009-d9c3d2aca920">Thread Local Storage</a>).


<div class="alert"><b>Note</b>  The multi-threaded apartment is intended for use by non-GUI threads. Threads in multi-threaded apartments should not perform UI actions. This is because UI threads require a message pump, and COM does not pump messages for threads in a multi-threaded apartment.</div>
<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>



<a href="https://msdn.microsoft.com/bdef4089-93e6-4845-8dcc-1150d7a0d033">IInitializeSpy::PostInitialize</a>



<a href="https://msdn.microsoft.com/f5b345d1-ab37-401a-9cb4-b01ef7254fc8">IInitializeSpy::PreInitialize</a>



<a href="https://msdn.microsoft.com/cb62412a-d079-40f9-89dc-cce0bf3889af">Processes, Threads, and Apartments</a>
 

 

