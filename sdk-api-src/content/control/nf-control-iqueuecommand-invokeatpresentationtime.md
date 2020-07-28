---
UID: NF:control.IQueueCommand.InvokeAtPresentationTime
title: IQueueCommand::InvokeAtPresentationTime (control.h)
description: The InvokeAtPresentationTime method queues a method to be invoked at the specified presentation time.
helpviewer_keywords: ["IQueueCommand interface [DirectShow]","InvokeAtPresentationTime method","IQueueCommand.InvokeAtPresentationTime","IQueueCommand::InvokeAtPresentationTime","IQueueCommandInvokeAtPresentationTime","InvokeAtPresentationTime","InvokeAtPresentationTime method [DirectShow]","InvokeAtPresentationTime method [DirectShow]","IQueueCommand interface","control/IQueueCommand::InvokeAtPresentationTime","dshow.iqueuecommand_invokeatpresentationtime"]
old-location: dshow\iqueuecommand_invokeatpresentationtime.htm
tech.root: dshow
ms.assetid: 95255a18-d6e3-4970-90cb-c87629560ff6
ms.date: 12/05/2018
ms.keywords: IQueueCommand interface [DirectShow],InvokeAtPresentationTime method, IQueueCommand.InvokeAtPresentationTime, IQueueCommand::InvokeAtPresentationTime, IQueueCommandInvokeAtPresentationTime, InvokeAtPresentationTime, InvokeAtPresentationTime method [DirectShow], InvokeAtPresentationTime method [DirectShow],IQueueCommand interface, control/IQueueCommand::InvokeAtPresentationTime, dshow.iqueuecommand_invokeatpresentationtime
f1_keywords:
- control/IQueueCommand.InvokeAtPresentationTime
dev_langs:
- c++
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IQueueCommand.InvokeAtPresentationTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IQueueCommand::InvokeAtPresentationTime


## -description



The <code>InvokeAtPresentationTime</code> method queues a method to be invoked at the specified presentation time.




## -parameters




### -param pCmd [out]

Address of a variable that receives an <a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-ideferredcommand">IDeferredCommand</a> interface pointer.


### -param time [in]

Time at which to invoke the command.


### -param iid [in]

Pointer to the interface identifier (IID) of interface.


### -param dispidMethod [in]

Dispatch identifier (DISPID) of a method or property on the interface. Equivalent to the <i>dispIdMember</i> parameter of the <b>IDispatch::Invoke</b> method.


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


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Use the <b>IDispatch::GetIDsOfNames</b> method to retrieve the DISPID for the <i>dispidMember</i> parameter.

For a code example, see <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-iqueuecommand-invokeatstreamtime">IQueueCommand::InvokeAtStreamTime</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-iqueuecommand">IQueueCommand Interface</a>
 

 

