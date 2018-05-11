---
UID: NF:control.IMediaEvent.CancelDefaultHandling
title: IMediaEvent::CancelDefaultHandling
author: windows-driver-content
description: The CancelDefaultHandling method cancels the Filter Graph Manager's default handling for a specified event. The event notification is passed to the application.
old-location: dshow\imediaevent_canceldefaulthandling.htm
old-project: DirectShow
ms.assetid: 955d0494-8418-42a1-ab6e-2c779165f578
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: CancelDefaultHandling, CancelDefaultHandling method [DirectShow], CancelDefaultHandling method [DirectShow],IMediaEvent interface, IMediaEvent interface [DirectShow],CancelDefaultHandling method, IMediaEvent.CancelDefaultHandling, IMediaEvent::CancelDefaultHandling, IMediaEventCancelDefaultHandling, control/IMediaEvent::CancelDefaultHandling, dshow.imediaevent_canceldefaulthandling
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: WMPContextMenuInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IMediaEvent.CancelDefaultHandling
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IMediaEvent::CancelDefaultHandling


## -description



The <code>CancelDefaultHandling</code> method cancels the Filter Graph Manager's default handling for a specified event. The event notification is passed to the application.




## -parameters




### -param lEvCode

Event code for which to cancel default handling.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

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



To restore the default handling for an event, call the <a href="https://msdn.microsoft.com/2df616b0-b944-44ab-8147-4f70796dd2a2">IMediaEvent::RestoreDefaultHandling</a> method with the event code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/651561d1-4e7e-48de-9cba-769ddb553e63">IMediaEvent Interface</a>
 

 

