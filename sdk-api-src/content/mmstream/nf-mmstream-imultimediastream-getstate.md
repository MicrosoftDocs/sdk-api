---
UID: NF:mmstream.IMultiMediaStream.GetState
title: IMultiMediaStream::GetState (mmstream.h)
description: Note  This interface is deprecated. New applications should not use it. The GetState method retrieves the current state of the multimedia stream object.
helpviewer_keywords: ["GetState","GetState method [DirectShow]","GetState method [DirectShow]","IMultiMediaStream interface","IMultiMediaStream interface [DirectShow]","GetState method","IMultiMediaStream.GetState","IMultiMediaStream::GetState","IMultiMediaStreamGetState","dshow.imultimediastream_getstate","mmstream/IMultiMediaStream::GetState"]
old-location: dshow\imultimediastream_getstate.htm
tech.root: dshow
ms.assetid: 8d01c4cf-2de9-4e9c-8b6e-921284f4f1b6
ms.date: 12/05/2018
ms.keywords: GetState, GetState method [DirectShow], GetState method [DirectShow],IMultiMediaStream interface, IMultiMediaStream interface [DirectShow],GetState method, IMultiMediaStream.GetState, IMultiMediaStream::GetState, IMultiMediaStreamGetState, dshow.imultimediastream_getstate, mmstream/IMultiMediaStream::GetState
req.header: mmstream.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IMultiMediaStream::GetState
 - mmstream/IMultiMediaStream::GetState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mmstream.h
api_name:
 - IMultiMediaStream.GetState
---

# IMultiMediaStream::GetState


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetState</code> method retrieves the current state of the multimedia stream object.

## -parameters

### -param pCurrentState [out]

Pointer to a variable that receives a member of the <a href="/previous-versions/windows/desktop/api/mmstream/ne-mmstream-stream_state">STREAM_STATE</a> enumeration.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-imultimediastream">IMultiMediaStream Interface</a>