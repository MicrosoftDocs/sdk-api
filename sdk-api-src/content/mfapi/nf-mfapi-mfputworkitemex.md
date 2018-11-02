---
UID: NF:mfapi.MFPutWorkItemEx
title: MFPutWorkItemEx function
author: windows-sdk-content
description: Puts an asynchronous operation on a work queue.
old-location: mf\mfputworkitemex.htm
tech.root: medfound
ms.assetid: 67b4f7c6-0d49-4ed0-9bc3-e583451884af
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 67b4f7c6-0d49-4ed0-9bc3-e583451884af, MFPutWorkItemEx, MFPutWorkItemEx function [Media Foundation], mf.mfputworkitemex, mfapi/MFPutWorkItemEx
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFPutWorkItemEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFPutWorkItemEx function


## -description


Puts an asynchronous operation on a work queue.
        


## -parameters




### -param dwQueue [in]

The identifier for the work queue. This value can specify one of the standard Media Foundation work queues, or a work queue created by the application. For list of standard Media Foundation work queues, see <a href="https://msdn.microsoft.com/c769f876-83ca-4b04-a054-22fa7146310e">Work Queue Identifiers</a>. To create a new work queue, call <a href="https://msdn.microsoft.com/8def4375-919c-4619-9484-9ce2708a3886">MFAllocateWorkQueue</a> or <a href="https://msdn.microsoft.com/422b8bc2-0616-4f7f-9908-775940f8c1ab">MFAllocateWorkQueueEx</a>.
          


### -param pResult [in]

A pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface of an asynchronous result object. To create the result object, call <a href="https://msdn.microsoft.com/6ff773a9-961e-4a5e-ad37-46234022c575">MFCreateAsyncResult</a>.
          


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
Invalid work queue identifier. For more information, see <a href="https://msdn.microsoft.com/374dd139-d3e7-45d0-a7d3-1187b928ef57">IMFAsyncCallback::GetParameters</a>.

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



To invoke the work-item, this function passes <i>pResult</i> to the <a href="https://msdn.microsoft.com/28832d50-9b15-4eb0-96f9-2032d4edcaf4">MFInvokeCallback</a> function. The callback is specified when you create the result object specified by <i>pResult</i>.
      

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/b0233589-2a55-4803-9dcb-85d757734dee">MFPutWorkItem</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

