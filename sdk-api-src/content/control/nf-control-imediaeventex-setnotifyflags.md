---
UID: NF:control.IMediaEventEx.SetNotifyFlags
title: IMediaEventEx::SetNotifyFlags
author: windows-driver-content
description: The SetNotifyFlags method enables or disables event notifications.
old-location: dshow\imediaeventex_setnotifyflags.htm
old-project: DirectShow
ms.assetid: 6a41b6eb-3fe9-4b2e-bcbb-a407e0e6ab5e
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IMediaEventEx interface [DirectShow],SetNotifyFlags method, IMediaEventEx.SetNotifyFlags, IMediaEventEx::SetNotifyFlags, IMediaEventExSetNotifyFlags, SetNotifyFlags, SetNotifyFlags method [DirectShow], SetNotifyFlags method [DirectShow],IMediaEventEx interface, control/IMediaEventEx::SetNotifyFlags, dshow.imediaeventex_setnotifyflags
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
-	IMediaEventEx.SetNotifyFlags
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
<th>
                  Value
                </th>
<th>
                  Description
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

If event notifications are disabled, the handle returned by the <a href="https://msdn.microsoft.com/83db8d24-d872-4a90-a896-1cc51273b551">IMediaEvent::GetEventHandle</a> method is signaled at the end of each stream—that is, whenever the Filter Graph Manager receives an <a href="https://msdn.microsoft.com/46037d53-085d-4fd0-91a0-408702cbfce5">EC_COMPLETE</a> event.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9d367b0a-c7ec-49d4-a41e-045ac81d2c51">IMediaEventEx Interface</a>
 

 

