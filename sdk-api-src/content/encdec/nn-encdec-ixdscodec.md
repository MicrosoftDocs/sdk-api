---
UID: NN:encdec.IXDSCodec
title: IXDSCodec (encdec.h)
author: windows-sdk-content
description: The IXDSCodec interface is exposed by the XDS Codec filter. Most applications will not have to use this interface.
old-location: mstv\ixdscodec.htm
tech.root: mstv
ms.assetid: c34a3418-2ae5-45a6-9e3b-2bd7cf33d44b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXDSCodec, IXDSCodec interface [Microsoft TV Technologies], IXDSCodec interface [Microsoft TV Technologies],described, IXDSCodecInterface, encdec/IXDSCodec, mstv.ixdscodec
ms.topic: interface
f1_keywords: 
 - "encdec/IXDSCodec"
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
 - IXDSCodec
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXDSCodec interface


## -description



The <b>IXDSCodec</b> interface is exposed by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/xds-codec-filter">XDS Codec</a> filter. Most applications will not have to use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXDSCodec</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXDSCodec</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXDSCodec</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-ixdscodec-get_ccsubstreamservice">get_CCSubstreamService</a>
</td>
<td align="left" width="63%">
Queries which line 21 data channels the XDS Codec filter sends to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/xdstorat-object">XDSToRat</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-ixdscodec-get_xdstoratobjok">get_XDSToRatObjOK</a>
</td>
<td align="left" width="63%">
Queries whether the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/xdstorat-object">XDSToRat</a> object was created successfully.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-ixdscodec-getcontentadvisoryrating">GetContentAdvisoryRating</a>
</td>
<td align="left" width="63%">
Retrieves the most recent ratings information parsed by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/xdstorat-object">XDSToRat</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-ixdscodec-getcurrlicenseexpdate">GetCurrLicenseExpDate</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-ixdscodec-getlasterrorcode">GetLastErrorCode</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-ixdscodec-getxdspacket">GetXDSPacket</a>
</td>
<td align="left" width="63%">
Retrieves the most recent XDS packet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-ixdscodec-put_ccsubstreamservice">put_CCSubstreamService</a>
</td>
<td align="left" width="63%">
Specifies which line 21 data channels the XDS Codec filter sends to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/xdstorat-object">XDSToRat</a> object.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IXDSCodec)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tv-ratings-interfaces">TV Ratings Interfaces</a>
 

 

