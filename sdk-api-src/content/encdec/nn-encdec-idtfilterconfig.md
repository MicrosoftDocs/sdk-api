---
UID: NN:encdec.IDTFilterConfig
title: IDTFilterConfig (encdec.h)
author: windows-sdk-content
description: The IDTFilterConfig interface configures the Decrypter/Detagger filter. Most applications will not have to use this interface.
old-location: mstv\idtfilterconfig.htm
tech.root: mstv
ms.assetid: 1f6d7969-3207-48f8-8972-0a95287ccc71
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDTFilterConfig, IDTFilterConfig interface [Microsoft TV Technologies], IDTFilterConfig interface [Microsoft TV Technologies],described, IDTFilterConfigInterface, encdec/IDTFilterConfig, mstv.idtfilterconfig
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
 - IDTFilterConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDTFilterConfig interface


## -description



The <b>IDTFilterConfig</b> interface configures the Decrypter/Detagger filter. Most applications will not have to use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDTFilterConfig</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDTFilterConfig</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-idtfilterconfig-getsecurechannelobject">GetSecureChannelObject</a>
</td>
<td align="left" width="63%">
Retrieves the secure channel object used to decrypt the stream.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDTFilterConfig)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tv-ratings-interfaces">TV Ratings Interfaces</a>
 

 

