---
UID: NF:mfapi.MFCreateAsyncResult
title: MFCreateAsyncResult function (mfapi.h)
description: Creates an asynchronous result object. Use this function if you are implementing an asynchronous method. (MFCreateAsyncResult)
helpviewer_keywords: ["6ff773a9-961e-4a5e-ad37-46234022c575","MFCreateAsyncResult","MFCreateAsyncResult function [Media Foundation]","mf.mfcreateasyncresult","mfapi/MFCreateAsyncResult"]
old-location: mf\mfcreateasyncresult.htm
tech.root: mf
ms.assetid: 6ff773a9-961e-4a5e-ad37-46234022c575
ms.date: 12/05/2018
ms.keywords: 6ff773a9-961e-4a5e-ad37-46234022c575, MFCreateAsyncResult, MFCreateAsyncResult function [Media Foundation], mf.mfcreateasyncresult, mfapi/MFCreateAsyncResult
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
 - MFCreateAsyncResult
 - mfapi/MFCreateAsyncResult
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
 - MFCreateAsyncResult
---

# MFCreateAsyncResult function


## -description

Creates an asynchronous result object. Use this function if you are implementing an asynchronous method.

## -parameters

### -param punkObject

Pointer to the object stored in the asynchronous result. This pointer is returned by the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject">IMFAsyncResult::GetObject</a> method. This parameter can be <b>NULL</b>.

### -param pCallback

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface. This interface is implemented by the caller of the asynchronous method.

### -param punkState

Pointer to the <b>IUnknown</b> interface of a state object. This value is provided by the caller of the asynchronous method. This parameter can be <b>NULL</b>.

### -param ppAsyncResult

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. The caller must release the interface.

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

To invoke the callback specified in <i>pCallback</i>, call the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback">MFInvokeCallback</a> function.

## -see-also

<a href="/windows/desktop/medfound/asynchronous-callback-methods">Asynchronous Callback Methods</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
