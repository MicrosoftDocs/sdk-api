---
UID: NF:rtworkq.IRtwqAsyncResult.GetStatus
title: IRtwqAsyncResult::GetStatus (rtworkq.h)
description: Returns the status of the asynchronous operation. (IRtwqAsyncResult.GetStatus)
helpviewer_keywords: ["GetStatus","GetStatus method","GetStatus method","IRtwqAsyncResult interface","IRtwqAsyncResult interface","GetStatus method","IRtwqAsyncResult.GetStatus","IRtwqAsyncResult::GetStatus","base.irtwqasyncresult_getstatus","rtworkq/IRtwqAsyncResult::GetStatus"]
old-location: base\irtwqasyncresult_getstatus.htm
tech.root: backup
ms.assetid: 90E965E5-29E6-4FC9-A923-FBBCC12195E2
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method, GetStatus method,IRtwqAsyncResult interface, IRtwqAsyncResult interface,GetStatus method, IRtwqAsyncResult.GetStatus, IRtwqAsyncResult::GetStatus, base.irtwqasyncresult_getstatus, rtworkq/IRtwqAsyncResult::GetStatus
req.header: rtworkq.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRtwqAsyncResult::GetStatus
 - rtworkq/IRtwqAsyncResult::GetStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTWorkQ.dll
api_name:
 - IRtwqAsyncResult.GetStatus
---

# IRtwqAsyncResult::GetStatus


## -description

Returns the status of the asynchronous operation.



## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The operation completed successfully.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rtworkq/nn-rtworkq-irtwqasyncresult">IRtwqAsyncResult</a>
