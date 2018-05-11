---
UID: NN:strmif.IGetCapabilitiesKey
title: IGetCapabilitiesKey
author: windows-driver-content
description: The IGetCapabilitiesKey interface enables an application to retrieve the capabilities of a software or hardware codec from the registry, without creating an instance of the encoder filter.
old-location: dshow\igetcapabilitieskey.htm
old-project: DirectShow
ms.assetid: 97a9112f-7b7b-4a7e-8f40-bdb148d413c8
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IGetCapabilitiesKey, IGetCapabilitiesKey interface [DirectShow], IGetCapabilitiesKey interface [DirectShow],described, IGetCapabilitiesKeyInterface, dshow.igetcapabilitieskey, strmif/IGetCapabilitiesKey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
-	IGetCapabilitiesKey
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IGetCapabilitiesKey interface


## -description



The <b>IGetCapabilitiesKey</b> interface enables an application to retrieve the capabilities of a software or hardware codec from the registry, without creating an instance of the encoder filter. The moniker for the codec filter exposes this interface. For more information, see <a href="https://msdn.microsoft.com/3d19152f-17a3-4576-a2a2-5b827d9ca8d1">Encoder API</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGetCapabilitiesKey</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGetCapabilitiesKey</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGetCapabilitiesKey</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02c3edfe-9ce1-4d9f-bdd1-79e818b43800">GetCapabilitiesKey</a>
</td>
<td align="left" width="63%">
Gets a registry key that contains the capabilities information for the codec.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

