---
UID: NF:mfapi.MFPutWorkItem2
title: MFPutWorkItem2 function (mfapi.h)
description: Puts an asynchronous operation on a work queue, with a specified priority.helpviewer_keywords: ["MFPutWorkItem2","MFPutWorkItem2 function [Media Foundation]","mf.mfputworkitem2","mfapi/MFPutWorkItem2"]
old-location: mf\mfputworkitem2.htm
tech.root: medfound
ms.assetid: C49818B3-83FF-40CE-B68A-F60F3277F7B8
ms.date: 12/05/2018
ms.keywords: MFPutWorkItem2, MFPutWorkItem2 function [Media Foundation], mf.mfputworkitem2, mfapi/MFPutWorkItem2
f1_keywords:
- mfapi/MFPutWorkItem2
dev_langs:
- c++
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
- MFPutWorkItem2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFPutWorkItem2 function


## -description


Puts an asynchronous operation on a work queue, with a specified priority.


## -parameters




### -param dwQueue [in]

The identifier for the work queue. This value can specify one of the standard Media Foundation work queues, or a work queue created by the application. For list of standard Media Foundation work queues, see <a href="https://docs.microsoft.com/windows/desktop/medfound/work-queue-identifiers">Work Queue Identifiers</a>. To create a new work queue, call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue">MFAllocateWorkQueue</a> or  MFAllocateWorkQueueEx.
          


### -param Priority [in]

The priority of the work item. Work items are performed in order of priority.


### -param pCallback [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface. The caller must implement this interface.
          


### -param pState [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.
          


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
Invalid work queue identifier.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfstartup">MFStartup</a> function was not called, or <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfshutdown">MFShutdown</a> was called.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-work-queue-and-threading-improvements">Work Queue and Threading Improvements</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/work-queues">Work Queues</a>
 

 

