---
UID: NN:encdec.IXDSCodecConfig
title: IXDSCodecConfig (encdec.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005. The IXDSCodecConfig interface configures the XDS Codec filter. Most applications will not have to use this interface.
old-location: mstv\ixdscodecconfig.htm
tech.root: mstv
ms.assetid: 90f8ce9b-2a85-43d0-9f2a-a3d248414a2d
ms.date: 12/05/2018
ms.keywords: IXDSCodecConfig, IXDSCodecConfig interface [Microsoft TV Technologies], IXDSCodecConfig interface [Microsoft TV Technologies],described, IXDSCodecConfigInterface, encdec/IXDSCodecConfig, mstv.ixdscodecconfig
ms.topic: interface
f1_keywords:
- encdec/IXDSCodecConfig
dev_langs:
- c++
req.header: encdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
- encdec.h
api_name:
- IXDSCodecConfig
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXDSCodecConfig interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        

The <b>IXDSCodecConfig</b> interface configures the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/xds-codec-filter">XDS Codec</a> filter. Most applications will not have to use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXDSCodecConfig</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXDSCodecConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXDSCodecConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-ixdscodecconfig-getsecurechannelobject">GetSecureChannelObject</a>
</td>
<td align="left" width="63%">
Retrieves the secure channel object used to decrypt the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-ixdscodecconfig-setpausebuffertime">SetPauseBufferTime</a>
</td>
<td align="left" width="63%">
Specifies how often the XDS Codec filter attempts to generate a new license.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IXDSCodecConfig)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tv-ratings-interfaces">TV Ratings Interfaces</a>
 

 

