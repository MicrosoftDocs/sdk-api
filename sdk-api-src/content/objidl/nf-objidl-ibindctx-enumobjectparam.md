---
UID: NF:objidl.IBindCtx.EnumObjectParam
title: IBindCtx::EnumObjectParam
author: windows-sdk-content
description: Retrieves a pointer to an interface that can be used to enumerate the keys of the bind context's string-keyed table of pointers.
old-location: com\ibindctx_enumobjectparam.htm
old-project: com
ms.assetid: 9e799ce4-e9b3-4b31-98a0-2167a0c19848
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EnumObjectParam, EnumObjectParam method [COM], EnumObjectParam method [COM],IBindCtx interface, IBindCtx interface [COM],EnumObjectParam method, IBindCtx.EnumObjectParam, IBindCtx::EnumObjectParam, _com_ibindctx_enumobjectparam, com.ibindctx_enumobjectparam, objidl/IBindCtx::EnumObjectParam
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IBindCtx.EnumObjectParam
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IBindCtx::EnumObjectParam


## -description


Retrieves a pointer to an interface that can be used to enumerate the keys of the bind context's string-keyed table of pointers.


## -parameters




### -param ppenum [out]

The address of an <a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a>* pointer variable that receives the interface pointer to the enumerator. If an error occurs, *<i>ppenum</i> is set to <b>NULL</b>. If *<i>ppenum</i> is non-<b>NULL</b>, the implementation calls <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on *<i>ppenum</i>; it is the caller's responsibility to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a>.


## -returns



This method can return the standard return values E_OUTOFMEMORY and S_OK.




## -remarks



The keys returned by the enumerator are the ones previously specified in calls to <a href="https://msdn.microsoft.com/7ee2b5b2-9b9c-41f1-8e58-7432ebc0f9ed">IBindCtx::RegisterObjectParam</a>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A bind context maintains a table of interface pointers, each associated with a string key. This enables communication between a moniker implementation and the caller that initiated the binding operation. One party can store an interface pointer under a string known to both parties so that the other party can later retrieve it from the bind context.

In the system implementation of the <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> interface, this method is not implemented. Therefore, calling this method results in a return value of E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>



<a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a>
 

 

