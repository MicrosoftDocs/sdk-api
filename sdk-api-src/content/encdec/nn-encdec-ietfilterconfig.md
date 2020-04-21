---
UID: NN:encdec.IETFilterConfig
title: IETFilterConfig (encdec.h)
description: The IETFilterConfig interface configures the Encrypter/Tagger filter. Most applications will not have to use this interface.helpviewer_keywords: ["IETFilterConfig","IETFilterConfig interface [Microsoft TV Technologies]","IETFilterConfig interface [Microsoft TV Technologies]","described","IETFilterConfigInterface","encdec/IETFilterConfig","mstv.ietfilterconfig"]
old-location: mstv\ietfilterconfig.htm
tech.root: mstv
ms.assetid: 6fa3da1b-863b-4ed7-b5ef-4ed1c05d2456
ms.date: 12/05/2018
ms.keywords: IETFilterConfig, IETFilterConfig interface [Microsoft TV Technologies], IETFilterConfig interface [Microsoft TV Technologies],described, IETFilterConfigInterface, encdec/IETFilterConfig, mstv.ietfilterconfig
f1_keywords:
- encdec/IETFilterConfig
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IETFilterConfig interface


## -description



The <b>IETFilterConfig</b> interface configures the Encrypter/Tagger filter. Most applications will not have to use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IETFilterConfig</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IETFilterConfig</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-ietfilterconfig-getsecurechannelobject">GetSecureChannelObject</a>
</td>
<td align="left" width="63%">
Retrieves the secure channel object used to encrypt the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-ietfilterconfig-initlicense">InitLicense</a>
</td>
<td align="left" width="63%">
Initializes an encryption license.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IETFilterConfig)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tv-ratings-interfaces">TV Ratings Interfaces</a>
 

 

