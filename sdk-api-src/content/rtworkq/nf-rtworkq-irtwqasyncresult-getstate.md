---
UID: NF:rtworkq.IRtwqAsyncResult.GetState
title: IRtwqAsyncResult::GetState (rtworkq.h)
description: Returns the state object specified by the caller in the asynchronous Begin method. (IRtwqAsyncResult.GetState)
helpviewer_keywords: ["GetState","GetState method","GetState method","IRtwqAsyncResult interface","IRtwqAsyncResult interface","GetState method","IRtwqAsyncResult.GetState","IRtwqAsyncResult::GetState","base.irtwqasyncresult_getstate","rtworkq/IRtwqAsyncResult::GetState"]
old-location: base\irtwqasyncresult_getstate.htm
tech.root: backup
ms.assetid: 26940ECA-BE6A-42E4-8D9E-E002A6D5DD23
ms.date: 12/05/2018
ms.keywords: GetState, GetState method, GetState method,IRtwqAsyncResult interface, IRtwqAsyncResult interface,GetState method, IRtwqAsyncResult.GetState, IRtwqAsyncResult::GetState, base.irtwqasyncresult_getstate, rtworkq/IRtwqAsyncResult::GetState
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
 - IRtwqAsyncResult::GetState
 - rtworkq/IRtwqAsyncResult::GetState
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
 - IRtwqAsyncResult.GetState
---

# IRtwqAsyncResult::GetState


## -description

Returns the state object specified by the caller in the asynchronous <b>Begin</b> method.

## -parameters

### -param ppunkState [out]

Receives a pointer to the state object's <b>IUnknown</b> interface. If the value is not <b>NULL</b>, the caller must release the interface.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
There is no state object associated with this asynchronous result.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rtworkq/nn-rtworkq-irtwqasyncresult">IRtwqAsyncResult</a>
