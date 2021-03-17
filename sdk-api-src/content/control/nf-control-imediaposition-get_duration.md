---
UID: NF:control.IMediaPosition.get_Duration
title: IMediaPosition::get_Duration (control.h)
description: The get_Duration method retrieves the duration of the stream.
helpviewer_keywords: ["IMediaPosition interface [DirectShow]","get_Duration method","IMediaPosition.get_Duration","IMediaPosition::get_Duration","IMediaPositionget_Duration","control/IMediaPosition::get_Duration","dshow.imediaposition_get_duration","get_Duration","get_Duration method [DirectShow]","get_Duration method [DirectShow]","IMediaPosition interface"]
old-location: dshow\imediaposition_get_duration.htm
tech.root: dshow
ms.assetid: 9971ca0e-a16d-4227-9efa-c965d501e6ef
ms.date: 12/05/2018
ms.keywords: IMediaPosition interface [DirectShow],get_Duration method, IMediaPosition.get_Duration, IMediaPosition::get_Duration, IMediaPositionget_Duration, control/IMediaPosition::get_Duration, dshow.imediaposition_get_duration, get_Duration, get_Duration method [DirectShow], get_Duration method [DirectShow],IMediaPosition interface
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaPosition::get_Duration
 - control/IMediaPosition::get_Duration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMediaPosition.get_Duration
---

# IMediaPosition::get_Duration


## -description

The <code>get_Duration</code> method retrieves the duration of the stream.

## -parameters

### -param plength [out]

Pointer to a variable that receives the total stream length, in seconds.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
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
</table>

## -remarks

This method retrieves the duration of the stream at normal playback speed. Changing the playback rate does not affect the duration.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-imediaposition">IMediaPosition Interface</a>