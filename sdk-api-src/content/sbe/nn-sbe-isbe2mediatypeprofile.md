---
UID: NN:sbe.ISBE2MediaTypeProfile
title: ISBE2MediaTypeProfile (sbe.h)
description: Implements a media type profile.
helpviewer_keywords: ["ISBE2MediaTypeProfile","ISBE2MediaTypeProfile interface [Microsoft TV Technologies]","ISBE2MediaTypeProfile interface [Microsoft TV Technologies]","described","mstv.isbe2mediatypeprofile","sbe/ISBE2MediaTypeProfile"]
old-location: mstv\isbe2mediatypeprofile.htm
tech.root: mstv
ms.assetid: b2fb3d08-cbef-4dbf-a60b-8363ccee4fbf
ms.date: 12/05/2018
ms.keywords: ISBE2MediaTypeProfile, ISBE2MediaTypeProfile interface [Microsoft TV Technologies], ISBE2MediaTypeProfile interface [Microsoft TV Technologies],described, mstv.isbe2mediatypeprofile, sbe/ISBE2MediaTypeProfile
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISBE2MediaTypeProfile
 - sbe/ISBE2MediaTypeProfile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbe.dll
api_name:
 - ISBE2MediaTypeProfile
---

# ISBE2MediaTypeProfile interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Implements a media type profile. A <i>media type profile</i> describes a set of streams and their media types, which are used when output pins for a <a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filter are created to specify the media types supported by those pins. The Stream Buffer Source filter implements the <a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2crossbar">ISBE2Crossbar</a> interface, which you can use to set the media type profile for the filter. 

To obtain a pointer to the <b>ISBE2MediaTypeProfile</b>  interface, call the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2crossbar-getinitialprofile">ISBE2Crossbar::GetInitialProfile</a> method for the crossbar, and then use the value returned in the  <i>ppProfile</i> output parameter.

## -inheritance

The <b>ISBE2MediaTypeProfile</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISBE2MediaTypeProfile</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ISBE2MediaTypeProfile)</code>.
