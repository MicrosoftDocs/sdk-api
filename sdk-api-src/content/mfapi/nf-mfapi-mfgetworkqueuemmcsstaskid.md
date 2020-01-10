---
UID: NF:mfapi.MFGetWorkQueueMMCSSTaskId
title: MFGetWorkQueueMMCSSTaskId function (mfapi.h)
description: Retrieves the Multimedia Class Scheduler Service (MMCSS) task identifier currently associated with this work queue.
old-location: mf\mfgetworkqueuemmcsstaskid.htm
tech.root: medfound
ms.assetid: e9b2eea8-2ed3-4b08-ad2a-c8ee2e09f3e4
ms.date: 12/05/2018
ms.keywords: MFGetWorkQueueMMCSSTaskId, MFGetWorkQueueMMCSSTaskId function [Media Foundation], e9b2eea8-2ed3-4b08-ad2a-c8ee2e09f3e4, mf.mfgetworkqueuemmcsstaskid, mfapi/MFGetWorkQueueMMCSSTaskId
f1_keywords:
- mfapi/MFGetWorkQueueMMCSSTaskId
dev_langs:
- c++
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
- MFGetWorkQueueMMCSSTaskId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFGetWorkQueueMMCSSTaskId function


## -description



Retrieves the Multimedia Class Scheduler Service (MMCSS) task identifier currently associated with this work queue.




## -parameters




### -param dwWorkQueueId [in]

Identifier for the work queue. The identifier is retrieved by the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue">MFAllocateWorkQueue</a> function.


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



To associate a work queue with an MMCSS task, call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcss">MFBeginRegisterWorkQueueWithMMCSS</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/work-queues">Work Queues</a>
 

 

