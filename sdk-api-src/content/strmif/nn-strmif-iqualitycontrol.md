---
UID: NN:strmif.IQualityControl
title: IQualityControl
author: windows-driver-content
description: The IQualityControl interface provides support for quality control.
old-location: dshow\iqualitycontrol.htm
old-project: DirectShow
ms.assetid: 2672e563-75d7-4a8a-b914-7b0712e856e8
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IQualityControl, IQualityControl interface [DirectShow], IQualityControl interface [DirectShow],described, IQualityControlInterface, dshow.iqualitycontrol, strmif/IQualityControl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: strmif.h
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IQualityControl
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IQualityControl interface


## -description



The <code>IQualityControl</code> interface provides support for quality control. An object exposes this interface if it can generate or receive quality-control messages. This includes renderer filters (which typically generate quality control messages), pins (which receive them), and external quality managers (which also receive them).

A renderer filter generates a quality-control message by calling the <a href="https://msdn.microsoft.com/c7a34356-b0b2-49c1-bdc2-d8043fdc2862">IQualityControl::Notify</a> method on the output pin of the upstream filter. The upstream filter either handles the message or passes it upstream.

An application can implement its own quality-control manager. Call <a href="https://msdn.microsoft.com/f82922dc-ec33-499d-b052-a1ba38632c52">IQualityControl::SetSink</a> on the renderer to designate the quality-control manager as the recipient for quality-control messages. Calling this method overrides the default handling of quality-control messages.

However, most applications will not implement their own quality-control managers; and aside from this special case, applications typically do not use this interface. For more information, see <a href="https://msdn.microsoft.com/b1def588-6c9c-4853-a69b-1ba5df8b5ba2">Quality-Control Management</a>





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IQualityControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IQualityControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IQualityControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7a34356-b0b2-49c1-bdc2-d8043fdc2862">Notify</a>
</td>
<td align="left" width="63%">
Notifies the recipient that a quality change is requested.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f82922dc-ec33-499d-b052-a1ba38632c52">SetSink</a>
</td>
<td align="left" width="63%">
Sets the <code>IQualityControl</code> object that will receive quality messages.

</td>
</tr>
</table> 

