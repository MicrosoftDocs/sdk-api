---
UID: NN:encdec.IETFilterConfig
title: IETFilterConfig
author: windows-sdk-content
description: The IETFilterConfig interface configures the Encrypter/Tagger filter. Most applications will not have to use this interface.
old-location: mstv\ietfilterconfig.htm
tech.root: mstv
ms.assetid: 6fa3da1b-863b-4ed7-b5ef-4ed1c05d2456
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IETFilterConfig, IETFilterConfig interface [Microsoft TV Technologies], IETFilterConfig interface [Microsoft TV Technologies],described, IETFilterConfigInterface, encdec/IETFilterConfig, mstv.ietfilterconfig
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EncDec.h
api_name:
 - IETFilterConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IETFilterConfig interface


## -description



The <b>IETFilterConfig</b> interface configures the Encrypter/Tagger filter. Most applications will not have to use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IETFilterConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IETFilterConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IETFilterConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/385f4525-97b0-4973-8b74-a05816e43556">GetSecureChannelObject</a>
</td>
<td align="left" width="63%">
Retrieves the secure channel object used to encrypt the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d88d9ee0-1748-43e4-90d4-671b1449ef03">InitLicense</a>
</td>
<td align="left" width="63%">
Initializes an encryption license.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IETFilterConfig)</code>.




## -see-also




<a href="https://msdn.microsoft.com/abe939a3-5f43-4fdf-9d4d-34b7be8893eb">TV Ratings Interfaces</a>
 

 

