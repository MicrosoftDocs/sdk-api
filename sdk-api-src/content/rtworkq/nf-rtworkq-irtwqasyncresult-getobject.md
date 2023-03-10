---
UID: NF:rtworkq.IRtwqAsyncResult.GetObject
title: IRtwqAsyncResult::GetObject (rtworkq.h)
description: Returns an object associated with the asynchronous operation. The type of object, if any, depends on the asynchronous method that was called. (IRtwqAsyncResult.GetObject)
helpviewer_keywords: ["GetObject","GetObject method","GetObject method","IRtwqAsyncResult interface","IRtwqAsyncResult interface","GetObject method","IRtwqAsyncResult.GetObject","IRtwqAsyncResult::GetObject","base.irtwqasyncresult_getobject","rtworkq/IRtwqAsyncResult::GetObject"]
old-location: base\irtwqasyncresult_getobject.htm
tech.root: backup
ms.assetid: EF872EDD-4263-4835-81E4-0A61F18E9202
ms.date: 12/05/2018
ms.keywords: GetObject, GetObject method, GetObject method,IRtwqAsyncResult interface, IRtwqAsyncResult interface,GetObject method, IRtwqAsyncResult.GetObject, IRtwqAsyncResult::GetObject, base.irtwqasyncresult_getobject, rtworkq/IRtwqAsyncResult::GetObject
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
 - IRtwqAsyncResult::GetObject
 - rtworkq/IRtwqAsyncResult::GetObject
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
 - IRtwqAsyncResult.GetObject
---

# IRtwqAsyncResult::GetObject


## -description

Returns an object associated with the asynchronous operation. The type of object, if any, depends on the asynchronous method that was called.

## -parameters

### -param ppObject [out]

Receives a pointer to the object's <b>IUnknown</b> interface. If no object is associated with the operation, this parameter receives the value <b>NULL</b>. If the value is not <b>NULL</b>, the caller must release the interface.

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
There is no object associated with this asynchronous result.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rtworkq/nn-rtworkq-irtwqasyncresult">IRtwqAsyncResult</a>
