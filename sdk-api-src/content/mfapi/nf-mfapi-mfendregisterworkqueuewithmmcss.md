---
UID: NF:mfapi.MFEndRegisterWorkQueueWithMMCSS
title: MFEndRegisterWorkQueueWithMMCSS function
author: windows-sdk-content
description: Completes an asynchronous request to associate a work queue with a Multimedia Class Scheduler Service (MMCSS) task.
old-location: mf\mfendregisterworkqueuewithmmcss.htm
tech.root: medfound
ms.assetid: 42d71e1a-a538-45d3-bbf4-1835db15bff9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 42d71e1a-a538-45d3-bbf4-1835db15bff9, MFEndRegisterWorkQueueWithMMCSS, MFEndRegisterWorkQueueWithMMCSS function [Media Foundation], mf.mfendregisterworkqueuewithmmcss, mfapi/MFEndRegisterWorkQueueWithMMCSS
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
 - MFEndRegisterWorkQueueWithMMCSS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MFEndRegisterWorkQueueWithMMCSS
: 
---

# MFEndRegisterWorkQueueWithMMCSS function


## -description



Completes an asynchronous request to associate a work queue with a Multimedia Class Scheduler Service (MMCSS) task.




## -parameters




### -param pResult [in]

Pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method.


### -param pdwTaskId [in]

The unique task identifier.


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



Call this function when the <a href="https://msdn.microsoft.com/9bcc6ab3-b7da-4b32-a868-c16f83ce20ca">MFBeginRegisterWorkQueueWithMMCSS</a> function completes asynchronously.

To unregister the work queue from the MMCSS class, call <a href="https://msdn.microsoft.com/e164785f-9899-45f0-805f-b091508e35aa">MFBeginUnregisterWorkQueueWithMMCSS</a>.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

