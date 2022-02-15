---
UID: NN:mfidl.IMFContentEnabler
title: IMFContentEnabler (mfidl.h)
description: Implements one step that must be performed for the user to access media content.
helpviewer_keywords: ["45d02bd0-1104-47ec-8559-8cc51590fc62","IMFContentEnabler","IMFContentEnabler interface [Media Foundation]","IMFContentEnabler interface [Media Foundation]","described","mf.imfcontentenabler","mfidl/IMFContentEnabler"]
old-location: mf\imfcontentenabler.htm
tech.root: mf
ms.assetid: 45d02bd0-1104-47ec-8559-8cc51590fc62
ms.date: 12/05/2018
ms.keywords: 45d02bd0-1104-47ec-8559-8cc51590fc62, IMFContentEnabler, IMFContentEnabler interface [Media Foundation], IMFContentEnabler interface [Media Foundation],described, mf.imfcontentenabler, mfidl/IMFContentEnabler
req.header: mfidl.h
req.include-header: 
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
 - IMFContentEnabler
 - mfidl/IMFContentEnabler
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
 - IMFContentEnabler
---

# IMFContentEnabler interface


## -description

Implements one step that must be performed for the user to access media content. For example, the steps might be individualization followed by license acquisition. Each of these steps would be encapsulated by a content enabler object that exposes the <b>IMFContentEnabler</b> interface.

## -inheritance

The <b>IMFContentEnabler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFContentEnabler</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/how-to-play-protected-media-files">How to Play Protected Media Files</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
