---
UID: NN:ocidl.IQuickActivate
title: IQuickActivate (ocidl.h)
description: Enables controls and containers to avoid performance bottlenecks on loading controls. It combines the load-time or initialization-time handshaking between the control and its container into a single call.
helpviewer_keywords: ["IQuickActivate","IQuickActivate interface [COM]","IQuickActivate interface [COM]","described","_ctrl_iquickactivate","com.iquickactivate","ocidl/IQuickActivate"]
old-location: com\iquickactivate.htm
tech.root: com
ms.assetid: 9b3e3b56-5055-4dfa-83e6-702578662463
ms.date: 12/05/2018
ms.keywords: IQuickActivate, IQuickActivate interface [COM], IQuickActivate interface [COM],described, _ctrl_iquickactivate, com.iquickactivate, ocidl/IQuickActivate
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IQuickActivate
 - ocidl/IQuickActivate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IQuickActivate
---

# IQuickActivate interface


## -description

Enables controls and containers to avoid performance bottlenecks on loading controls. It combines the load-time or initialization-time handshaking between the control and its container into a single call.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IQuickActivate</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IQuickActivate</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iquickactivate-getcontentextent">GetContentExtent</a>
</td>
<td align="left" width="63%">
Gets the content extent of a control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iquickactivate-quickactivate">QuickActivate</a>
</td>
<td align="left" width="63%">
Quick activates a control.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iquickactivate-setcontentextent">SetContentExtent</a>
</td>
<td align="left" width="63%">
Sets the content extent of a control.

</td>
</tr>
</table>

