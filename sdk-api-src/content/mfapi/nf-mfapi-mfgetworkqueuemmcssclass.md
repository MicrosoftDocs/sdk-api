---
UID: NF:mfapi.MFGetWorkQueueMMCSSClass
title: MFGetWorkQueueMMCSSClass function (mfapi.h)
author: windows-sdk-content
description: Retrieves the Multimedia Class Scheduler Service (MMCSS) class currently associated with this work queue.
old-location: mf\mfgetworkqueuemmcssclass.htm
tech.root: medfound
ms.assetid: 97b48d18-3844-4b97-9bab-c5fc38eb927e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 97b48d18-3844-4b97-9bab-c5fc38eb927e, MFGetWorkQueueMMCSSClass, MFGetWorkQueueMMCSSClass function [Media Foundation], mf.mfgetworkqueuemmcssclass, mfapi/MFGetWorkQueueMMCSSClass
ms.topic: function
f1_keywords: 
 - "mfapi/MFGetWorkQueueMMCSSClass"
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
 - MFGetWorkQueueMMCSSClass
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFGetWorkQueueMMCSSClass function


## -description



Retrieves the Multimedia Class Scheduler Service (MMCSS) class currently associated with this work queue.




## -parameters




### -param dwWorkQueueId [in]

Identifier for the work queue. The identifier is retrieved by the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue">MFAllocateWorkQueue</a> function.


### -param pwszClass [out]

Pointer to a buffer that receives the name of the MMCSS class. This parameter can be <b>NULL</b>.


### -param pcchClass [in, out]

On input, specifies the size of the <i>pwszClass</i> buffer, in characters. On output, receives the required size of the buffer, in characters. The size includes the terminating null character.


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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwszClass</i> buffer is too small to receive the task name.

</td>
</tr>
</table>
 




## -remarks



If the work queue is not associated with an MMCSS task, the function retrieves an empty string.

To associate a work queue with an MMCSS task, call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcss">MFBeginRegisterWorkQueueWithMMCSS</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/work-queues">Work Queues</a>
 

 

