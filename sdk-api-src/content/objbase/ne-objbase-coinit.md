---
UID: NE:objbase.tagCOINIT
title: COINIT (objbase.h)
description: Determines the concurrency model used for incoming calls to objects created by this thread. This concurrency model can be either apartment-threaded or multithreaded.
helpviewer_keywords: ["COINIT","COINIT enumeration [COM]","COINIT_APARTMENTTHREADED","COINIT_DISABLE_OLE1DDE","COINIT_MULTITHREADED","COINIT_SPEED_OVER_MEMORY","_com_COINIT","com.coinit","objbase/COINIT","objbase/COINIT_APARTMENTTHREADED","objbase/COINIT_DISABLE_OLE1DDE","objbase/COINIT_MULTITHREADED","objbase/COINIT_SPEED_OVER_MEMORY"]
old-location: com\coinit.htm
tech.root: com
ms.assetid: 0ac4a809-05f8-46d7-8e79-9d4e88b487f4
ms.date: 12/05/2018
ms.keywords: COINIT, COINIT enumeration [COM], COINIT_APARTMENTTHREADED, COINIT_DISABLE_OLE1DDE, COINIT_MULTITHREADED, COINIT_SPEED_OVER_MEMORY, _com_COINIT, com.coinit, objbase/COINIT, objbase/COINIT_APARTMENTTHREADED, objbase/COINIT_DISABLE_OLE1DDE, objbase/COINIT_MULTITHREADED, objbase/COINIT_SPEED_OVER_MEMORY
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: COINIT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCOINIT
 - objbase/tagCOINIT
 - COINIT
 - objbase/COINIT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objbase.h
api_name:
 - COINIT
---

# COINIT enumeration


## -description

Determines the concurrency model used for incoming calls to objects created by this thread. This concurrency model can be either apartment-threaded or multithreaded.

## -enum-fields

### -field COINIT_APARTMENTTHREADED:0x2

Initializes the thread for apartment-threaded object concurrency (see Remarks).

### -field COINIT_MULTITHREADED

Initializes the thread for multithreaded object concurrency (see Remarks).

### -field COINIT_DISABLE_OLE1DDE:0x4

Disables DDE for OLE1 support.

### -field COINIT_SPEED_OVER_MEMORY:0x8

Increase memory usage in an attempt to increase performance.

## -remarks

When a thread is initialized through a call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a>, you choose whether to initialize it as apartment-threaded or multithreaded by designating one of the members of <b>COINIT</b> as its second parameter. This designates how incoming calls to any object created by that thread are handled, that is, the object's concurrency.

Apartment-threading, while allowing for multiple threads of execution, serializes all incoming calls by requiring that calls to methods of objects created by this thread always run on the same thread, i.e. the apartment/thread that created them. In addition, calls can arrive only at message-queue boundaries. Because of this serialization, it is not typically necessary to write concurrency control into the code for the object, other than to avoid calls to <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> and <a href="/previous-versions/windows/desktop/oe/oe-ihttpmailtransport-sendmessage">SendMessage</a> during processing that must not be interrupted by other method invocations or calls to other objects in the same apartment/thread.



Multi-threading (also called free-threading) allows calls to methods of objects created by this thread to be run on any thread. There is no serialization of calls, i.e. many calls may occur to the same method or to the same object or simultaneously. Multi-threaded object concurrency offers the highest performance and takes the best advantage of multiprocessor hardware for cross-thread, cross-process, and cross-machine calling, since calls to objects are not serialized in any way. This means, however, that the code for objects must enforce its own concurrency model, typically through the use of synchronization primitives, such as critical sections, semaphores, or mutexes. In addition, because the object doesn't control the lifetime of the threads that are accessing it, no thread-specific state may be stored in the object (in <a href="/windows/desktop/ProcThread/thread-local-storage">Thread Local Storage</a>).


<div class="alert"><b>Note</b>  The multi-threaded apartment is intended for use by non-GUI threads. Threads in multi-threaded apartments should not perform UI actions. This is because UI threads require a message pump, and COM does not pump messages for threads in a multi-threaded apartment.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a>



<a href="/windows/desktop/api/objidl/nf-objidl-iinitializespy-postinitialize">IInitializeSpy::PostInitialize</a>



<a href="/windows/desktop/api/objidl/nf-objidl-iinitializespy-preinitialize">IInitializeSpy::PreInitialize</a>



<a href="/windows/desktop/com/processes--threads--and-apartments">Processes, Threads, and Apartments</a>
