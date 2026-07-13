---
UID: NF:rtworkq.IRtwqAsyncResult.SetStatus
title: IRtwqAsyncResult::SetStatus (rtworkq.h)
description: Sets the status of the asynchronous operation. (IRtwqAsyncResult.SetStatus)
helpviewer_keywords: ["IRtwqAsyncResult interface","SetStatus method","IRtwqAsyncResult.SetStatus","IRtwqAsyncResult::SetStatus","SetStatus","SetStatus method","SetStatus method","IRtwqAsyncResult interface","base.irtwqasyncresult_setstatus","rtworkq/IRtwqAsyncResult::SetStatus"]
old-location: base\irtwqasyncresult_setstatus.htm
tech.root: backup
ms.assetid: 9F3A74F5-615B-40B2-8E69-145D0ECA22A9
ms.date: 12/05/2018
ms.keywords: IRtwqAsyncResult interface,SetStatus method, IRtwqAsyncResult.SetStatus, IRtwqAsyncResult::SetStatus, SetStatus, SetStatus method, SetStatus method,IRtwqAsyncResult interface, base.irtwqasyncresult_setstatus, rtworkq/IRtwqAsyncResult::SetStatus
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
 - IRtwqAsyncResult::SetStatus
 - rtworkq/IRtwqAsyncResult::SetStatus
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
 - IRtwqAsyncResult.SetStatus
---

# IRtwqAsyncResult::SetStatus


## -description

Sets the status of the asynchronous operation.

## -parameters

### -param hrStatus [in]

The status of the asynchronous operation.

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
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rtworkq/nn-rtworkq-irtwqasyncresult">IRtwqAsyncResult</a>
