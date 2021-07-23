---
UID: NN:mfobjects.IMFMediaType
title: IMFMediaType (mfobjects.h)
description: Represents a description of a media format.
helpviewer_keywords: ["IMFMediaType","IMFMediaType interface [Media Foundation]","IMFMediaType interface [Media Foundation]","described","f1d60bec-71e4-4fcc-a020-92754b6f3c02","mf.imfmediatype","mfobjects/IMFMediaType"]
old-location: mf\imfmediatype.htm
tech.root: mf
ms.assetid: f1d60bec-71e4-4fcc-a020-92754b6f3c02
ms.date: 12/05/2018
ms.keywords: IMFMediaType, IMFMediaType interface [Media Foundation], IMFMediaType interface [Media Foundation],described, f1d60bec-71e4-4fcc-a020-92754b6f3c02, mf.imfmediatype, mfobjects/IMFMediaType
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaType
 - mfobjects/IMFMediaType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaType
---

# IMFMediaType interface


## -description

Represents a description of a media format.

## -inheritance

The <b>IMFMediaType</b> interface inherits from <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>. <b>IMFMediaType</b> also has these types of members:

## -remarks

To create a new media type, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype">MFCreateMediaType</a>.
      

All of the information in a media type is stored as attributes. To clone a media type, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems">IMFAttributes::CopyAllItems</a>.
      

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/media-type-attributes">Media Type Attributes</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>
