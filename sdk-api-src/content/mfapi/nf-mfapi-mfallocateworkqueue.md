---
UID: NF:mfapi.MFAllocateWorkQueue
title: MFAllocateWorkQueue function (mfapi.h)
description: Creates a new work queue. (MFAllocateWorkQueue)
helpviewer_keywords: ["8def4375-919c-4619-9484-9ce2708a3886","MFAllocateWorkQueue","MFAllocateWorkQueue function [Media Foundation]","mf.mfallocateworkqueue","mfapi/MFAllocateWorkQueue"]
old-location: mf\mfallocateworkqueue.htm
tech.root: mf
ms.assetid: 8def4375-919c-4619-9484-9ce2708a3886
ms.date: 12/05/2018
ms.keywords: 8def4375-919c-4619-9484-9ce2708a3886, MFAllocateWorkQueue, MFAllocateWorkQueue function [Media Foundation], mf.mfallocateworkqueue, mfapi/MFAllocateWorkQueue
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFAllocateWorkQueue
 - mfapi/MFAllocateWorkQueue
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
 - MFAllocateWorkQueue
---

# MFAllocateWorkQueue function


## -description

Creates a new work queue.

## -parameters

### -param pdwWorkQueue [out]

Receives an identifier for the work queue.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The application exceeded the maximum number of work queues.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The application did not call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfstartup">MFStartup</a>, or the application has already called <a href="/windows/desktop/api/mfapi/nf-mfapi-mfshutdown">MFShutdown</a>.
              

</td>
</tr>
</table>

## -remarks

When you are done using the work queue, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfunlockworkqueue">MFUnlockWorkQueue</a>.

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem">MFPutWorkItem</a>



<a href="/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex">MFPutWorkItemEx</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>
