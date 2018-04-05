---
UID: NN:ksproxy.IKsPin
title: IKsPin
author: windows-driver-content
description: The IKsPin interface provides a method to retrieve the mediums supported by a pin on a kernel-mode filter. IKsPin has additional methods besides the one shown here, but they are not supported for DirectShow.
old-location: dshow\ikspin.htm
old-project: DirectShow
ms.assetid: 14d9bef2-e8f0-49d5-bd89-69a95814cf8c
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IKsPin, IKsPin interface [DirectShow], IKsPin interface [DirectShow], described, IKsPinInterface, dshow.ikspin, ksproxy/IKsPin
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: ksproxy.h
req.include-header: 
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
req.typenames: WAVEFORMATEXTENSIBLE, *PWAVEFORMATEXTENSIBLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IKsPin
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IKsPin interface


## -description



The <code>IKsPin</code> interface provides a method to retrieve the mediums supported by a pin on a kernel-mode filter. <code>IKsPin</code> has additional methods besides the one shown here, but they are not supported for DirectShow.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IKsPin</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IKsPin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IKsPin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/554bf968-6054-4f9d-95db-facf0444641f">KsQueryMediums</a>
</td>
<td align="left" width="63%">
Retrieves the mediums supported by a pin.

</td>
</tr>
</table> 


## -remarks



You must include Ks.h before Ksproxy.h.



