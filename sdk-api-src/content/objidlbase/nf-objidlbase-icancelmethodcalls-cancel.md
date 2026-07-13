---
UID: NF:objidlbase.ICancelMethodCalls.Cancel
title: ICancelMethodCalls::Cancel (objidlbase.h)
description: The ICancelMethodCalls::Cancel (objidlbase.h) method requests that a method call be canceled.
helpviewer_keywords: ["Cancel","Cancel method [COM]","Cancel method [COM]","ICancelMethodCalls interface","ICancelMethodCalls interface [COM]","Cancel method","ICancelMethodCalls.Cancel","ICancelMethodCalls::Cancel","_com_icancelmethodcalls_cancel","com.icancelmethodcalls_cancel","objidlbase/ICancelMethodCalls::Cancel"]
old-location: com\icancelmethodcalls_cancel.htm
tech.root: com
ms.assetid: 3c3fdcec-10f1-4fbf-af93-582e7390decf
ms.date: 08/13/2022
ms.keywords: Cancel, Cancel method [COM], Cancel method [COM],ICancelMethodCalls interface, ICancelMethodCalls interface [COM],Cancel method, ICancelMethodCalls.Cancel, ICancelMethodCalls::Cancel, _com_icancelmethodcalls_cancel, com.icancelmethodcalls_cancel, objidlbase/ICancelMethodCalls::Cancel
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICancelMethodCalls::Cancel
 - objidlbase/ICancelMethodCalls::Cancel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - ICancelMethodCalls.Cancel
---

# ICancelMethodCalls::Cancel


## -description

Requests that a method call be canceled.

## -parameters

### -param ulSeconds [in]

The number of seconds to wait for the server to complete the outbound call after the client requests cancellation.

## -returns

This method can return one of these values.

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
The cancellation request was made.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_CALL_CANCELED</b></dt>
</dl>
</td>
<td width="60%">
The call was already canceled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_CANCEL_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
Call cancellation is not enabled on the thread that is processing the call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_E_CALL_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The call was completed during the timeout interval.


</td>
</tr>
</table>

## -remarks

The <b>Cancel</b> method only issues a cancel request. A return value of S_OK does not mean that the call was canceled, only that an attempt was made to cancel the call. The behavior of the cancel object on receiving a cancel request is entirely at the discretion of the implementer.

If a method that returns an <b>HRESULT</b> is canceled, the return value will be RPC_S_CALL_CANCELED.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-icancelmethodcalls">ICancelMethodCalls</a>
