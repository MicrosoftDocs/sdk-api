---
UID: NN:ocidl.IQuickActivate
title: IQuickActivate
author: windows-sdk-content
description: Enables controls and containers to avoid performance bottlenecks on loading controls. It combines the load-time or initialization-time handshaking between the control and its container into a single call.
old-location: com\iquickactivate.htm
old-project: com
ms.assetid: 9b3e3b56-5055-4dfa-83e6-702578662463
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: IQuickActivate, IQuickActivate interface [COM], IQuickActivate interface [COM],described, _ctrl_iquickactivate, com.iquickactivate, ocidl/IQuickActivate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IQuickActivate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IQuickActivate interface


## -description


Enables controls and containers to avoid performance bottlenecks on loading controls. It combines the load-time or initialization-time handshaking between the control and its container into a single call.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IQuickActivate</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IQuickActivate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IQuickActivate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ead9bf4d-44a1-4237-ad03-28a4253819b8">GetContentExtent</a>
</td>
<td align="left" width="63%">
Gets the content extent of a control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/504cb272-da1c-4ffb-b4b1-fdf288901660">QuickActivate</a>
</td>
<td align="left" width="63%">
Quick activates a control.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f763bd3-08b9-4804-8e52-2c8014428a45">SetContentExtent</a>
</td>
<td align="left" width="63%">
Sets the content extent of a control.

</td>
</tr>
</table> 

