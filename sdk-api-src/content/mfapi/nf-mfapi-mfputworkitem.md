---
UID: NF:mfapi.MFPutWorkItem
title: MFPutWorkItem function
author: windows-sdk-content
description: Puts an asynchronous operation on a work queue.
old-location: mf\mfputworkitem.htm
old-project: medfound
ms.assetid: b0233589-2a55-4803-9dcb-85d757734dee
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: MFPutWorkItem, MFPutWorkItem function [Media Foundation], b0233589-2a55-4803-9dcb-85d757734dee, mf.mfputworkitem, mfapi/MFPutWorkItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFPutWorkItem
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFPutWorkItem function


## -description



          Puts an asynchronous operation on a work queue.


## -parameters




### -param dwQueue [in]


            The identifier for the work queue. This value can specify one of the standard Media Foundation work queues, or a work queue created by the application. For list of standard Media Foundation work queues, see <a href="https://msdn.microsoft.com/c769f876-83ca-4b04-a054-22fa7146310e">Work Queue Identifiers</a>. To create a new work queue, call <a href="https://msdn.microsoft.com/8def4375-919c-4619-9484-9ce2708a3886">MFAllocateWorkQueue</a> or <a href="https://msdn.microsoft.com/422b8bc2-0616-4f7f-9908-775940f8c1ab">MFAllocateWorkQueueEx</a>.
          


### -param pCallback [in]


            A pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface. The caller must implement this interface.
          


### -param pState [in]

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.
          


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_INVALID_WORKQUEUE</b></b></dt>
</dl>
</td>
<td width="60%">
Invalid work queue. For more information, see <a href="https://msdn.microsoft.com/374dd139-d3e7-45d0-a7d3-1187b928ef57">IMFAsyncCallback::GetParameters</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/b4472e40-3681-4b26-9385-4df7bf19c2d8">MFStartup</a> function was not called, or <a href="https://msdn.microsoft.com/10be2361-b5b4-4c10-92a1-527ca22c74e4">MFShutdown</a> was called.

</td>
</tr>
</table>
 




## -remarks




        This function creates an asynchronous result object and puts the result object on the work queue. The work queue calls the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method specified by <i>pCallback</i>.
      




## -see-also




<a href="https://msdn.microsoft.com/67b4f7c6-0d49-4ed0-9bc3-e583451884af">MFPutWorkItemEx</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

