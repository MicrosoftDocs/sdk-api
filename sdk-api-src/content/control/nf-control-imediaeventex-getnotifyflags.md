---
UID: NF:control.IMediaEventEx.GetNotifyFlags
title: IMediaEventEx::GetNotifyFlags (control.h)
description: The GetNotifyFlags method determines whether event notifications are enabled.helpviewer_keywords: ["GetNotifyFlags","GetNotifyFlags method [DirectShow]","GetNotifyFlags method [DirectShow]","IMediaEventEx interface","IMediaEventEx interface [DirectShow]","GetNotifyFlags method","IMediaEventEx.GetNotifyFlags","IMediaEventEx::GetNotifyFlags","IMediaEventExGetNotifyFlags","control/IMediaEventEx::GetNotifyFlags","dshow.imediaeventex_getnotifyflags"]
old-location: dshow\imediaeventex_getnotifyflags.htm
tech.root: DirectShow
ms.assetid: 797c5ee2-5a3c-4e95-b4b8-e29b39460ee0
ms.date: 12/05/2018
ms.keywords: GetNotifyFlags, GetNotifyFlags method [DirectShow], GetNotifyFlags method [DirectShow],IMediaEventEx interface, IMediaEventEx interface [DirectShow],GetNotifyFlags method, IMediaEventEx.GetNotifyFlags, IMediaEventEx::GetNotifyFlags, IMediaEventExGetNotifyFlags, control/IMediaEventEx::GetNotifyFlags, dshow.imediaeventex_getnotifyflags
f1_keywords:
- control/IMediaEventEx.GetNotifyFlags
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
- IMediaEventEx.GetNotifyFlags
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaEventEx::GetNotifyFlags


## -description



The <code>GetNotifyFlags</code> method determines whether event notifications are enabled.




## -parameters




### -param lplNoNotifyFlags [out]

Pointer to a variable that receives one of the following values:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>Zero</td>
<td>Event notifications are enabled.</td>
</tr>
<tr>
<td>AM_MEDIAEVENT_NONOTIFY</td>
<td>Event notifications are disabled.</td>
</tr>
</table>
 


## -returns



Returns S_OK if successful, or E_POINTER if the <i>lplNoNotifyFlags</i> parameter is <b>NULL</b>.




## -remarks



By default, the Filter Graph Manager posts event notifications for the application. To disable event notification, call the <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediaeventex-setnotifyflags">IMediaEventEx::SetNotifyFlags</a> method with the value AM_MEDIAEVENT_NONOTIFY.

If event notifications are disabled, the handle returned by the <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediaevent-geteventhandle">IMediaEvent::GetEventHandle</a> method is signaled at the end of each stream—that is, whenever the Filter Graph Manager receives an <a href="https://docs.microsoft.com/windows/desktop/DirectShow/ec-complete">EC_COMPLETE</a> event.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-imediaeventex">IMediaEventEx Interface</a>
 

 

