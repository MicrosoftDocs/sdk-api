---
UID: NN:control.IMediaEventEx
title: IMediaEventEx
author: windows-sdk-content
description: The IMediaEventEx interface inherits the IMediaEvent interface, which contains methods for retrieving event notifications and for overriding the filter graph's default handling of events.
old-location: dshow\imediaeventex.htm
old-project: DirectShow
ms.assetid: 9d367b0a-c7ec-49d4-a41e-045ac81d2c51
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IMediaEventEx, IMediaEventEx interface [DirectShow], IMediaEventEx interface [DirectShow],described, IMediaEventExInterface, control/IMediaEventEx, dshow.imediaeventex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IMediaEventEx
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IMediaEventEx interface


## -description



The <b>IMediaEventEx</b> interface inherits the <a href="https://msdn.microsoft.com/651561d1-4e7e-48de-9cba-769ddb553e63">IMediaEvent</a> interface, which contains methods for retrieving event notifications and for overriding the filter graph's default handling of events. <b>IMediaEventEx</b> adds methods that enable an application window to receive messages when events occur. 

The Filter Graph Manager implements this interface.

For more information about event notification, see <a href="https://msdn.microsoft.com/301116a5-24e3-4c6d-8c80-bec77c7d62d7">Event Notification in DirectShow</a>. For a list of system-defined event notifications, see <a href="https://msdn.microsoft.com/339ffcd9-7724-4c92-b241-afbed81d9380">Event Notification Codes</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaEventEx</b> interface inherits from <a href="https://msdn.microsoft.com/651561d1-4e7e-48de-9cba-769ddb553e63">IMediaEvent</a>. <b>IMediaEventEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://msdn.microsoft.com/797c5ee2-5a3c-4e95-b4b8-e29b39460ee0">GetNotifyFlags</a>
</td>
<td align="left" width="63%">
Determines whether event notifications are enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a41b6eb-3fe9-4b2e-bcbb-a407e0e6ab5e">SetNotifyFlags</a>
</td>
<td align="left" width="63%">
Enables or disables event notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e582c79-b8c7-40be-97fd-75d5b7965570">SetNotifyWindow</a>
</td>
<td align="left" width="63%">
Registers a window to process event notifications.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/651561d1-4e7e-48de-9cba-769ddb553e63">IMediaEvent</a>
 

 

