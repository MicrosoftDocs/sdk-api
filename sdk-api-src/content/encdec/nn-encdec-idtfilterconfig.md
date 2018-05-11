---
UID: NN:encdec.IDTFilterConfig
title: IDTFilterConfig
author: windows-driver-content
description: The IDTFilterConfig interface configures the Decrypter/Detagger filter. Most applications will not have to use this interface.
old-location: mstv\idtfilterconfig.htm
old-project: mstv
ms.assetid: 1f6d7969-3207-48f8-8972-0a95287ccc71
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IDTFilterConfig, IDTFilterConfig interface [Microsoft TV Technologies], IDTFilterConfig interface [Microsoft TV Technologies],described, IDTFilterConfigInterface, encdec/IDTFilterConfig, mstv.idtfilterconfig
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: encdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ProtType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	EncDec.h
api_name:
-	IDTFilterConfig
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDTFilterConfig interface


## -description



The <b>IDTFilterConfig</b> interface configures the Decrypter/Detagger filter. Most applications will not have to use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDTFilterConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDTFilterConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDTFilterConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84057a08-b15f-4738-814d-c016507ac590">GetSecureChannelObject</a>
</td>
<td align="left" width="63%">
Retrieves the secure channel object used to decrypt the stream.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDTFilterConfig)</code>.




## -see-also




<a href="https://msdn.microsoft.com/abe939a3-5f43-4fdf-9d4d-34b7be8893eb">TV Ratings Interfaces</a>
 

 

