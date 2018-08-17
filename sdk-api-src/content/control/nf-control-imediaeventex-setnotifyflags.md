---
UID: NF:control.IMediaEventEx.SetNotifyFlags
title: IMediaEventEx::SetNotifyFlags
author: windows-sdk-content
description: The SetNotifyFlags method enables or disables event notifications.
old-location: dshow\imediaeventex_setnotifyflags.htm
old-project: DirectShow
ms.assetid: 6a41b6eb-3fe9-4b2e-bcbb-a407e0e6ab5e
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IMediaEventEx interface [DirectShow],SetNotifyFlags method, IMediaEventEx.SetNotifyFlags, IMediaEventEx::SetNotifyFlags, IMediaEventExSetNotifyFlags, SetNotifyFlags, SetNotifyFlags method [DirectShow], SetNotifyFlags method [DirectShow],IMediaEventEx interface, control/IMediaEventEx::SetNotifyFlags, dshow.imediaeventex_setnotifyflags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: control.h
req.include-header: Dshow.h
req.redist: 
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
tech.root: 
req.typenames: WMPContextMenuInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMediaEventEx.SetNotifyFlags
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IMediaEventEx::SetNotifyFlags


## -description



The <code>SetNotifyFlags</code> method enables or disables event notifications.




## -parameters




### -param lNoNotifyFlags [in]

Value indicating whether to enable or disable event notifications. Must be one of the following values:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>Zero</td>
<td>Enable event notifications.</td>
</tr>
<tr>
<td>AM_MEDIAEVENT_NONOTIFY</td>
<td>Disable event notifications.</td>
</tr>
</table>
 


## -returns



Returns S_OK if successful, or E_INVALIDARG if the <i>lNoNotifyFlags</i> parameter is invalid.




## -remarks



By default, the Filter Graph Manager posts event notifications for the application. If the <i>lNoNotifyFlags</i> parameter is AM_MEDIAEVENT_NONOTIFY, the Filter Graph Manager clears any pending event notifications from the queue, and does not post any new ones.

If event notifications are disabled, the handle returned by the <a href="https://msdn.microsoft.com/en-us/library/Dd406908(v=VS.85).aspx">IMediaEvent::GetEventHandle</a> method is signaled at the end of each stream—that is, whenever the Filter Graph Manager receives an <a href="https://msdn.microsoft.com/en-us/library/Dd319485(v=VS.85).aspx">EC_COMPLETE</a> event.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd406897(v=VS.85).aspx">IMediaEventEx Interface</a>
 

 

