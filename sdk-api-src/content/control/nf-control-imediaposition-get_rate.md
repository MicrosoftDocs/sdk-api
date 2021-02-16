---
UID: NF:control.IMediaPosition.get_Rate
title: IMediaPosition::get_Rate (control.h)
description: The get_Rate method retrieves the playback rate.
helpviewer_keywords: ["IMediaPosition interface [DirectShow]","get_Rate method","IMediaPosition.get_Rate","IMediaPosition::get_Rate","IMediaPositionget_Rate","control/IMediaPosition::get_Rate","dshow.imediaposition_get_rate","get_Rate","get_Rate method [DirectShow]","get_Rate method [DirectShow]","IMediaPosition interface"]
old-location: dshow\imediaposition_get_rate.htm
tech.root: dshow
ms.assetid: dbe18522-6adc-4a55-b74a-db05f619d40a
ms.date: 12/05/2018
ms.keywords: IMediaPosition interface [DirectShow],get_Rate method, IMediaPosition.get_Rate, IMediaPosition::get_Rate, IMediaPositionget_Rate, control/IMediaPosition::get_Rate, dshow.imediaposition_get_rate, get_Rate, get_Rate method [DirectShow], get_Rate method [DirectShow],IMediaPosition interface
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
 - IMediaPosition::get_Rate
 - control/IMediaPosition::get_Rate
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
 - IMediaPosition.get_Rate
---

# IMediaPosition::get_Rate


## -description

The <code>get_Rate</code> method retrieves the playback rate.

## -parameters

### -param pdRate [out]

Pointer to a variable that receives the playback rate.

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

The playback rate is expressed as a ratio of the normal speed. Thus, 1.0 is normal playback speed, 0.5 is half speed, and 2.0 is twice speed.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-imediaposition">IMediaPosition Interface</a>