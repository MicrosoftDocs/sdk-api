---
UID: NF:control.IMediaPosition.get_StopTime
title: IMediaPosition::get_StopTime (control.h)
description: The get_StopTime method retrieves the time at which the playback will stop, relative to the duration of the stream.
helpviewer_keywords: ["IMediaPosition interface [DirectShow]","get_StopTime method","IMediaPosition.get_StopTime","IMediaPosition::get_StopTime","IMediaPositionget_StopTime","control/IMediaPosition::get_StopTime","dshow.imediaposition_get_stoptime","get_StopTime","get_StopTime method [DirectShow]","get_StopTime method [DirectShow]","IMediaPosition interface"]
old-location: dshow\imediaposition_get_stoptime.htm
tech.root: dshow
ms.assetid: 6139ebb2-fad8-4394-9a5f-4753ca9fb143
ms.date: 12/05/2018
ms.keywords: IMediaPosition interface [DirectShow],get_StopTime method, IMediaPosition.get_StopTime, IMediaPosition::get_StopTime, IMediaPositionget_StopTime, control/IMediaPosition::get_StopTime, dshow.imediaposition_get_stoptime, get_StopTime, get_StopTime method [DirectShow], get_StopTime method [DirectShow],IMediaPosition interface
f1_keywords:
- control/IMediaPosition.get_StopTime
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IMediaPosition.get_StopTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaPosition::get_StopTime


## -description



The <code>get_StopTime</code> method retrieves the time at which the playback will stop, relative to the duration of the stream.




## -parameters




### -param pllTime [out]

Pointer to a variable that receives the stop time, in seconds.


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



The playback rate does not affect the value returned by this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-imediaposition">IMediaPosition Interface</a>
 

 

