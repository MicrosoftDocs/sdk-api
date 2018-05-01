---
UID: NF:control.IQueueCommand.InvokeAtPresentationTime
title: IQueueCommand::InvokeAtPresentationTime method
author: windows-driver-content
description: The InvokeAtPresentationTime method queues a method to be invoked at the specified presentation time.
old-location: dshow\iqueuecommand_invokeatpresentationtime.htm
old-project: DirectShow
ms.assetid: 95255a18-d6e3-4970-90cb-c87629560ff6
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IQueueCommand, IQueueCommand interface [DirectShow], InvokeAtPresentationTime method, IQueueCommand::InvokeAtPresentationTime, IQueueCommandInvokeAtPresentationTime, InvokeAtPresentationTime method [DirectShow], InvokeAtPresentationTime method [DirectShow], IQueueCommand interface, InvokeAtPresentationTime,IQueueCommand.InvokeAtPresentationTime, control/IQueueCommand::InvokeAtPresentationTime, dshow.iqueuecommand_invokeatpresentationtime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: control.h
req.include-header: Dshow.h
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
req.typenames: WMPContextMenuInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IQueueCommand.InvokeAtPresentationTime
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IQueueCommand::InvokeAtPresentationTime method


## -description



The <code>InvokeAtPresentationTime</code> method queues a method to be invoked at the specified presentation time.




## -parameters




### -param pCmd [out]

Address of a variable that receives an <a href="https://msdn.microsoft.com/8161932a-16aa-4700-b91d-b4d8948ad59f">IDeferredCommand</a> interface pointer.


### -param time [in]

Time at which to invoke the command.


### -param iid [in]

Pointer to the interface identifier (IID) of interface.


### -param dispidMethod




### -param wFlags [in]

Flags describing the context of the call. Equivalent to the <i>wFlags</i> parameter of the <b>IDispatch::Invoke</b> method.


### -param cArgs [in]

Number of arguments in <i>pDispParams</i>. Equivalent to the <b>cArgs</b> member of the <b>DISPPARAMS</b> structure.


### -param pDispParams [in]

Pointer to an array that contains the arguments. Equivalent to the <b>rgvarg</b> member of the <b>DISPPARAMS</b> structure.


### -param pvarResult [in, out]

Pointer a VARIANT that receives the result. Equivalent to the <i>pVarResult</i> parameter of the <b>IDispatch::Invoke</b> method.


### -param puArgErr [out]

Pointer to a variable that receives the index of the first argument that has an error. Equivalent to the <i>puArgErr</i> parameter of the <b>IDispatch::Invoke</b> method.


#### - dispidMember [in]

Dispatch identifier (DISPID) of a method or property on the interface. Equivalent to the <i>dispIdMember</i> parameter of the <b>IDispatch::Invoke</b> method.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Use the <b>IDispatch::GetIDsOfNames</b> method to retrieve the DISPID for the <i>dispidMember</i> parameter.

For a code example, see <a href="https://msdn.microsoft.com/350b6842-207c-47db-a3f8-9e2784d9da67">IQueueCommand::InvokeAtStreamTime</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/08efcbec-ce17-44e8-a3c1-4b5b95dcaaa4">IQueueCommand Interface</a>
 

 

