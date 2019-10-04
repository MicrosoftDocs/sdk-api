---
UID: NN:sbe.ISBE2MediaTypeProfile
title: ISBE2MediaTypeProfile (sbe.h)
author: windows-sdk-content
description: Implements a media type profile.
old-location: mstv\isbe2mediatypeprofile.htm
tech.root: mstv
ms.assetid: b2fb3d08-cbef-4dbf-a60b-8363ccee4fbf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISBE2MediaTypeProfile, ISBE2MediaTypeProfile interface [Microsoft TV Technologies], ISBE2MediaTypeProfile interface [Microsoft TV Technologies],described, mstv.isbe2mediatypeprofile, sbe/ISBE2MediaTypeProfile
ms.topic: interface
f1_keywords: 
 - "sbe/ISBE2MediaTypeProfile"
dev_langs:
 - c++
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Sbe.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbe.dll
api_name:
 - ISBE2MediaTypeProfile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISBE2MediaTypeProfile interface


## -description


Implements a media type profile. A <i>media type profile</i> describes a set of streams and their media types, which are used when output pins for a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filter are created to specify the media types supported by those pins. The Stream Buffer Source filter implements the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2crossbar">ISBE2Crossbar</a> interface, which you can use to set the media type profile for the filter. 

To obtain a pointer to the <b>ISBE2MediaTypeProfile</b>  interface, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2crossbar-getinitialprofile">ISBE2Crossbar::GetInitialProfile</a> method for the crossbar, and then use the value returned in the  <i>ppProfile</i> output parameter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISBE2MediaTypeProfile</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISBE2MediaTypeProfile</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISBE2MediaTypeProfile</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2mediatypeprofile-addstream">AddStream</a>
</td>
<td align="left" width="63%">
Adds a stream to the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2mediatypeprofile-deletestream">DeleteStream</a>
</td>
<td align="left" width="63%">
Removes a stream from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2mediatypeprofile-getstream">GetStream</a>
</td>
<td align="left" width="63%">
Gets the media type of a stream that is specified by its index in the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2mediatypeprofile-getstreamcount">GetStreamCount</a>
</td>
<td align="left" width="63%">
Gets the number of streams in the profile.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ISBE2MediaTypeProfile)</code>.



