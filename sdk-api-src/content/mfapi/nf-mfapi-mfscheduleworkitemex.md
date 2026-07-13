---
UID: NF:mfapi.MFScheduleWorkItemEx
title: MFScheduleWorkItemEx function (mfapi.h)
description: Schedules an asynchronous operation to be completed after a specified interval. (MFScheduleWorkItemEx)
helpviewer_keywords: ["MFScheduleWorkItemEx","MFScheduleWorkItemEx function [Media Foundation]","b698cae1-4f3b-4649-b6f7-583f223eb90c","mf.mfscheduleworkitemex","mfapi/MFScheduleWorkItemEx"]
old-location: mf\mfscheduleworkitemex.htm
tech.root: mf
ms.assetid: b698cae1-4f3b-4649-b6f7-583f223eb90c
ms.date: 12/05/2018
ms.keywords: MFScheduleWorkItemEx, MFScheduleWorkItemEx function [Media Foundation], b698cae1-4f3b-4649-b6f7-583f223eb90c, mf.mfscheduleworkitemex, mfapi/MFScheduleWorkItemEx
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFScheduleWorkItemEx
 - mfapi/MFScheduleWorkItemEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFScheduleWorkItemEx
---

# MFScheduleWorkItemEx function


## -description

Schedules an asynchronous operation to be completed after a specified interval.

## -parameters

### -param pResult [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface of an asynchronous result object. To create the result object, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult">MFCreateAsyncResult</a>.

### -param Timeout [in]

Time-out interval, in milliseconds. Set this parameter to a negative value. The callback is invoked after −<i>Timeout</i> milliseconds. For example, if <i>Timeout</i> is −5000, the callback is invoked after 5000 milliseconds.

### -param pKey [out]

Receives a key that can be used to cancel the timer. To cancel the timer, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcancelworkitem">MFCancelWorkItem</a> and pass this key in the <i>Key</i> parameter.

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

When the timer interval elapses, the timer calls <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback">MFInvokeCallback</a> with the <i>pResult</i> pointer to invoke the asynchronous callback. The callback is specified when you create the result object.

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem">MFScheduleWorkItem</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>
