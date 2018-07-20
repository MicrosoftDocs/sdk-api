---
UID: NF:mfapi.MFEndUnregisterWorkQueueWithMMCSS
title: MFEndUnregisterWorkQueueWithMMCSS function
author: windows-sdk-content
description: Completes an asynchronous request to unregister a work queue from a Multimedia Class Scheduler Service (MMCSS) task.
old-location: mf\mfendunregisterworkqueuewithmmcss.htm
old-project: medfound
ms.assetid: eca38d5d-9ca3-442e-80ca-96d8927178a1
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: MFEndUnregisterWorkQueueWithMMCSS, MFEndUnregisterWorkQueueWithMMCSS function [Media Foundation], eca38d5d-9ca3-442e-80ca-96d8927178a1, mf.mfendunregisterworkqueuewithmmcss, mfapi/MFEndUnregisterWorkQueueWithMMCSS
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
 - MFEndUnregisterWorkQueueWithMMCSS
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFEndUnregisterWorkQueueWithMMCSS function


## -description



Completes an asynchronous request to unregister a work queue from a Multimedia Class Scheduler Service (MMCSS) task.




## -parameters




### -param pResult [in]

Pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -remarks



Call this function when the <a href="https://msdn.microsoft.com/e164785f-9899-45f0-805f-b091508e35aa">MFBeginUnregisterWorkQueueWithMMCSS</a> function completes asynchronously.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

