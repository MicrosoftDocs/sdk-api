---
UID: NF:control.IMediaEvent.RestoreDefaultHandling
title: IMediaEvent::RestoreDefaultHandling (control.h)
description: The RestoreDefaultHandling method restores the Filter Graph Manager's default handling for a specified event.
helpviewer_keywords: ["IMediaEvent interface [DirectShow]","RestoreDefaultHandling method","IMediaEvent.RestoreDefaultHandling","IMediaEvent::RestoreDefaultHandling","IMediaEventRestoreDefaultHandling","RestoreDefaultHandling","RestoreDefaultHandling method [DirectShow]","RestoreDefaultHandling method [DirectShow]","IMediaEvent interface","control/IMediaEvent::RestoreDefaultHandling","dshow.imediaevent_restoredefaulthandling"]
old-location: dshow\imediaevent_restoredefaulthandling.htm
tech.root: dshow
ms.assetid: 2df616b0-b944-44ab-8147-4f70796dd2a2
ms.date: 12/05/2018
ms.keywords: IMediaEvent interface [DirectShow],RestoreDefaultHandling method, IMediaEvent.RestoreDefaultHandling, IMediaEvent::RestoreDefaultHandling, IMediaEventRestoreDefaultHandling, RestoreDefaultHandling, RestoreDefaultHandling method [DirectShow], RestoreDefaultHandling method [DirectShow],IMediaEvent interface, control/IMediaEvent::RestoreDefaultHandling, dshow.imediaevent_restoredefaulthandling
f1_keywords:
- control/IMediaEvent.RestoreDefaultHandling
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
- IMediaEvent.RestoreDefaultHandling
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaEvent::RestoreDefaultHandling


## -description



The <code>RestoreDefaultHandling</code> method restores the Filter Graph Manager's default handling for a specified event.




## -parameters




### -param lEvCode [in]

Event code for which to restore default handling.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
No default handling for this event.

</td>
</tr>
</table>
 




## -remarks



By default, the Filter Graph Manager handles some events (such as <a href="https://docs.microsoft.com/windows/desktop/DirectShow/ec-repaint">EC_REPAINT</a>) without passing them to the application. If you call the <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediaevent-canceldefaulthandling">IMediaEvent::CancelDefaultHandling</a> method to override the default handling for an event, you can restore the default behavior by calling <code>RestoreDefaultHandling</code> with the same event code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-imediaevent">IMediaEvent Interface</a>
 

 

