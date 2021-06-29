---
UID: NF:strmif.IDistributorNotify.Stop
title: IDistributorNotify::Stop (strmif.h)
description: The Stop method is called when the filter graph is entering a stopped state.
helpviewer_keywords: ["IDistributorNotify interface [DirectShow]","Stop method","IDistributorNotify.Stop","IDistributorNotify::Stop","IDistributorNotifyStop","Stop","Stop method [DirectShow]","Stop method [DirectShow]","IDistributorNotify interface","dshow.idistributornotify_stop","strmif/IDistributorNotify::Stop"]
old-location: dshow\idistributornotify_stop.htm
tech.root: dshow
ms.assetid: 21312954-bc48-402b-a03c-954c01b53231
ms.date: 12/05/2018
ms.keywords: IDistributorNotify interface [DirectShow],Stop method, IDistributorNotify.Stop, IDistributorNotify::Stop, IDistributorNotifyStop, Stop, Stop method [DirectShow], Stop method [DirectShow],IDistributorNotify interface, dshow.idistributornotify_stop, strmif/IDistributorNotify::Stop
req.header: strmif.h
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
 - IDistributorNotify::Stop
 - strmif/IDistributorNotify::Stop
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
 - IDistributorNotify.Stop
---

# IDistributorNotify::Stop


## -description

The <code>Stop</code> method is called when the filter graph is entering a stopped state.



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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Transition is not complete, but no error has occurred.

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

## -remarks

This method is called before the filters are notified.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idistributornotify">IDistributorNotify Interface</a>
