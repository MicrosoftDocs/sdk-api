---
UID: NF:control.IMediaEventEx.GetNotifyFlags
title: IMediaEventEx::GetNotifyFlags (control.h)
author: windows-sdk-content
description: The GetNotifyFlags method determines whether event notifications are enabled.
old-location: dshow\imediaeventex_getnotifyflags.htm
tech.root: DirectShow
ms.assetid: 797c5ee2-5a3c-4e95-b4b8-e29b39460ee0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetNotifyFlags, GetNotifyFlags method [DirectShow], GetNotifyFlags method [DirectShow],IMediaEventEx interface, IMediaEventEx interface [DirectShow],GetNotifyFlags method, IMediaEventEx.GetNotifyFlags, IMediaEventEx::GetNotifyFlags, IMediaEventExGetNotifyFlags, control/IMediaEventEx::GetNotifyFlags, dshow.imediaeventex_getnotifyflags
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
product: Windows
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



By default, the Filter Graph Manager posts event notifications for the application. To disable event notification, call the <a href="https://msdn.microsoft.com/en-us/library/Dd406899(v=VS.85).aspx">IMediaEventEx::SetNotifyFlags</a> method with the value AM_MEDIAEVENT_NONOTIFY.

If event notifications are disabled, the handle returned by the <a href="https://msdn.microsoft.com/en-us/library/Dd406908(v=VS.85).aspx">IMediaEvent::GetEventHandle</a> method is signaled at the end of each stream—that is, whenever the Filter Graph Manager receives an <a href="https://msdn.microsoft.com/46037d53-085d-4fd0-91a0-408702cbfce5">EC_COMPLETE</a> event.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd406897(v=VS.85).aspx">IMediaEventEx Interface</a>
 

 

