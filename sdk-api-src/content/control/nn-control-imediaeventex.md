---
UID: NN:control.IMediaEventEx
title: IMediaEventEx
author: windows-sdk-content
description: The IMediaEventEx interface inherits the IMediaEvent interface, which contains methods for retrieving event notifications and for overriding the filter graph's default handling of events.
old-location: dshow\imediaeventex.htm
tech.root: DirectShow
ms.assetid: 9d367b0a-c7ec-49d4-a41e-045ac81d2c51
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMediaEventEx, IMediaEventEx interface [DirectShow], IMediaEventEx interface [DirectShow],described, IMediaEventExInterface, control/IMediaEventEx, dshow.imediaeventex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IMediaEventEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaEventEx interface


## -description



The <b>IMediaEventEx</b> interface inherits the <a href="https://msdn.microsoft.com/en-us/library/Dd406896(v=VS.85).aspx">IMediaEvent</a> interface, which contains methods for retrieving event notifications and for overriding the filter graph's default handling of events. <b>IMediaEventEx</b> adds methods that enable an application window to receive messages when events occur. 

The Filter Graph Manager implements this interface.

For more information about event notification, see <a href="https://msdn.microsoft.com/en-us/library/Dd375626(v=VS.85).aspx">Event Notification in DirectShow</a>. For a list of system-defined event notifications, see <a href="https://msdn.microsoft.com/en-us/library/Dd375625(v=VS.85).aspx">Event Notification Codes</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaEventEx</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd406896(v=VS.85).aspx">IMediaEvent</a>. <b>IMediaEventEx</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IMediaEventEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406898(v=VS.85).aspx">GetNotifyFlags</a>
</td>
<td align="left" width="63%">
Determines whether event notifications are enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406899(v=VS.85).aspx">SetNotifyFlags</a>
</td>
<td align="left" width="63%">
Enables or disables event notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406900(v=VS.85).aspx">SetNotifyWindow</a>
</td>
<td align="left" width="63%">
Registers a window to process event notifications.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd406896(v=VS.85).aspx">IMediaEvent</a>
 

 

