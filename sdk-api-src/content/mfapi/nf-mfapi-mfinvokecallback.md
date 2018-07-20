---
UID: NF:mfapi.MFInvokeCallback
title: MFInvokeCallback function
author: windows-sdk-content
description: Invokes a callback method to complete an asynchronous operation.
old-location: mf\mfinvokecallback.htm
old-project: medfound
ms.assetid: 28832d50-9b15-4eb0-96f9-2032d4edcaf4
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: 28832d50-9b15-4eb0-96f9-2032d4edcaf4, MFInvokeCallback, MFInvokeCallback function [Media Foundation], mf.mfinvokecallback, mfapi/MFInvokeCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - MFInvokeCallback
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFInvokeCallback function


## -description



          Invokes a callback method to complete an asynchronous operation.
        


## -parameters




### -param pAsyncResult

Pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface. To create this object, call <a href="https://msdn.microsoft.com/6ff773a9-961e-4a5e-ad37-46234022c575">MFCreateAsyncResult</a>.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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

                The function succeeded.
              

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
<dt><b><b>MF_E_SHUTDOWN</b></b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/10be2361-b5b4-4c10-92a1-527ca22c74e4">MFShutdown</a> function was called to shut down the Media Foundation platform.

</td>
</tr>
</table>
 




## -remarks




        If you are implementing an asynchronous method, use this function to invoke the caller's <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method.

The callback is invoked from a Media Foundation work queue. For more information, see <a href="https://msdn.microsoft.com/cd94280d-7267-4d35-8333-aa4a5bd81b73">Writing an Asynchronous Method</a>.

The <a href="https://msdn.microsoft.com/10be2361-b5b4-4c10-92a1-527ca22c74e4">MFShutdown</a> function shuts down the work queue threads, so the callback is not guaranteed to be invoked after <b>MFShutdown</b> is called.




## -see-also




<a href="https://msdn.microsoft.com/ea778eaa-6460-4a93-bd6a-1857ea8b6230">Asynchronous Callback Methods</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

