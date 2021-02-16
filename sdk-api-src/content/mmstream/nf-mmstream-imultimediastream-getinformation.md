---
UID: NF:mmstream.IMultiMediaStream.GetInformation
title: IMultiMediaStream::GetInformation (mmstream.h)
description: Note  This interface is deprecated. New applications should not use it. The GetInformation method retrieves the capabilities of the multimedia stream object.
helpviewer_keywords: ["GetInformation","GetInformation method [DirectShow]","GetInformation method [DirectShow]","IMultiMediaStream interface","IMultiMediaStream interface [DirectShow]","GetInformation method","IMultiMediaStream.GetInformation","IMultiMediaStream::GetInformation","IMultiMediaStreamGetInformation","dshow.imultimediastream_getinformation","mmstream/IMultiMediaStream::GetInformation"]
old-location: dshow\imultimediastream_getinformation.htm
tech.root: dshow
ms.assetid: 27be6104-9ca4-48d7-aeda-5b633460e252
ms.date: 12/05/2018
ms.keywords: GetInformation, GetInformation method [DirectShow], GetInformation method [DirectShow],IMultiMediaStream interface, IMultiMediaStream interface [DirectShow],GetInformation method, IMultiMediaStream.GetInformation, IMultiMediaStream::GetInformation, IMultiMediaStreamGetInformation, dshow.imultimediastream_getinformation, mmstream/IMultiMediaStream::GetInformation
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
 - IMultiMediaStream::GetInformation
 - mmstream/IMultiMediaStream::GetInformation
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
 - IMultiMediaStream.GetInformation
---

# IMultiMediaStream::GetInformation


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetInformation</code> method retrieves the capabilities of the multimedia stream object.

## -parameters

### -param pdwFlags [out]

Pointer to a variable that receives a bitwise combination of the following flags.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>MMSSF_ASYNCHRONOUS</td>
<td>The object supports asynchronous sample updates. This flag is always returned.</td>
</tr>
<tr>
<td>MMSSF_HASCLOCK</td>
<td>The object has a clock.</td>
</tr>
<tr>
<td>MMSSF_SUPPORTSEEK</td>
<td>The object supports seeking.</td>
</tr>
</table>
 

This parameter can be <b>NULL</b>.

### -param pStreamType [out]

Pointer to a variable that receives a member of the <a href="/previous-versions/windows/desktop/api/mmstream/ne-mmstream-stream_type">STREAM_TYPE</a> enumeration. This value indicates whether the multimedia stream is read-only, write-only, or read/write. This parameter can be <b>NULL</b>.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error.

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