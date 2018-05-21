---
UID: NF:objidl.IBindCtx.GetRunningObjectTable
title: IBindCtx::GetRunningObjectTable
author: windows-driver-content
description: Retrieves an interface pointer to the running object table (ROT) for the computer on which this bind context is running.
old-location: com\ibindctx_getrunningobjecttable.htm
old-project: com
ms.assetid: 26938d07-d772-4e72-a6aa-57dd2f2cece1
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetRunningObjectTable, GetRunningObjectTable method [COM], GetRunningObjectTable method [COM],IBindCtx interface, IBindCtx interface [COM],GetRunningObjectTable method, IBindCtx.GetRunningObjectTable, IBindCtx::GetRunningObjectTable, _com_ibindctx_getrunningobjecttable, com.ibindctx_getrunningobjecttable, objidl/IBindCtx::GetRunningObjectTable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ObjIdl.h
api_name:
-	IBindCtx.GetRunningObjectTable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IBindCtx::GetRunningObjectTable


## -description


Retrieves an interface pointer to the running object table (ROT) for the computer on which this bind context is running.


## -parameters




### -param pprot [out]

The address of a <a href="https://msdn.microsoft.com/ff89bcb5-df6d-4325-b0e8-613217a68f42">IRunningObjectTable</a>* pointer variable that receives the interface pointer to the running object table. If an error occurs, *<i>pprot</i> is set to <b>NULL</b>. If *<i>pprot</i> is non-<b>NULL</b>, the implementation calls <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on the running table object; it is the caller's responsibility to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a>.


## -returns



This method can return the standard return values E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.




## -remarks



The running object table is a globally accessible table on each computer. It keeps track of all the objects that are currently running on the computer.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Typically, those implementing a new moniker class (through an implementation of <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface) call <b>GetRunningObjectTable</b>. It is useful to call this method in an implementation of <a href="https://msdn.microsoft.com/b5ce39ff-3387-4f72-9aea-5a26eed3810c">IMoniker::BindToObject</a> or <a href="https://msdn.microsoft.com/081b394c-1fe8-4519-999e-b3985a77bd9c">IMoniker::IsRunning</a> to check whether an object is currently running. You can also call this method in the implementation of <a href="https://msdn.microsoft.com/120cc951-6797-4ef6-890b-57ff8d3d23ba">IMoniker::GetTimeOfLastChange</a> to learn when a running object was last modified.

Moniker implementations should call this method instead of using the <b>GetRunningObjectTable</b> function. This makes it possible for future implementations of <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> to modify binding behavior.




## -see-also




<a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>



<a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>



<a href="https://msdn.microsoft.com/ff89bcb5-df6d-4325-b0e8-613217a68f42">IRunningObjectTable</a>
 

 

