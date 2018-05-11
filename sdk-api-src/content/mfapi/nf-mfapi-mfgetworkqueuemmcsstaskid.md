---
UID: NF:mfapi.MFGetWorkQueueMMCSSTaskId
title: MFGetWorkQueueMMCSSTaskId function
author: windows-driver-content
description: Retrieves the Multimedia Class Scheduler Service (MMCSS) task identifier currently associated with this work queue.
old-location: mf\mfgetworkqueuemmcsstaskid.htm
old-project: medfound
ms.assetid: e9b2eea8-2ed3-4b08-ad2a-c8ee2e09f3e4
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MFGetWorkQueueMMCSSTaskId, MFGetWorkQueueMMCSSTaskId function [Media Foundation], e9b2eea8-2ed3-4b08-ad2a-c8ee2e09f3e4, mf.mfgetworkqueuemmcsstaskid, mfapi/MFGetWorkQueueMMCSSTaskId
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
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mfplat.dll
api_name:
-	MFGetWorkQueueMMCSSTaskId
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFGetWorkQueueMMCSSTaskId function


## -description



Retrieves the Multimedia Class Scheduler Service (MMCSS) task identifier currently associated with this work queue.




## -parameters




### -param dwWorkQueueId [in]

Identifier for the work queue. The identifier is retrieved by the <a href="https://msdn.microsoft.com/8def4375-919c-4619-9484-9ce2708a3886">MFAllocateWorkQueue</a> function.


### -param pdwTaskId [out]

Receives the task identifier.


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



To associate a work queue with an MMCSS task, call <a href="https://msdn.microsoft.com/9bcc6ab3-b7da-4b32-a868-c16f83ce20ca">MFBeginRegisterWorkQueueWithMMCSS</a>.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

