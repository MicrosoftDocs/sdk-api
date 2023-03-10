---
UID: NF:oleidl.IOleCacheControl.OnStop
title: IOleCacheControl::OnStop (oleidl.h)
description: Notifies the cache that it should terminate any existing advise sinks. No indication is given as to whether a connection actually existed.
helpviewer_keywords: ["IOleCacheControl interface [COM]","OnStop method","IOleCacheControl.OnStop","IOleCacheControl::OnStop","OnStop","OnStop method [COM]","OnStop method [COM]","IOleCacheControl interface","_ole_iolecachecontrol_onstop","com.iolecachecontrol_onstop","oleidl/IOleCacheControl::OnStop"]
old-location: com\iolecachecontrol_onstop.htm
tech.root: com
ms.assetid: 95e62e9d-39bd-4bf8-ba25-c6a9c7fc515b
ms.date: 12/05/2018
ms.keywords: IOleCacheControl interface [COM],OnStop method, IOleCacheControl.OnStop, IOleCacheControl::OnStop, OnStop, OnStop method [COM], OnStop method [COM],IOleCacheControl interface, _ole_iolecachecontrol_onstop, com.iolecachecontrol_onstop, oleidl/IOleCacheControl::OnStop
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - IOleCacheControl::OnStop
 - oleidl/IOleCacheControl::OnStop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleCacheControl.OnStop
---

# IOleCacheControl::OnStop


## -description

Notifies the cache that it should terminate any existing advise sinks. No indication is given as to whether a connection actually existed.



## -returns

This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory is available for this operation.

</td>
</tr>
</table>

## -remarks

The data advisory connection between the running object and the cache is destroyed as part of calling <b>OnStop</b>.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-iolecachecontrol">IOleCacheControl</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolecachecontrol-onrun">IOleCacheControl::OnRun</a>
