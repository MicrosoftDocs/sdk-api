---
UID: NN:oleidl.IOleLink
title: IOleLink (oleidl.h)
description: Enables a linked object to provide its container with functions pertaining to linking.
helpviewer_keywords: ["IOleLink","IOleLink interface [COM]","IOleLink interface [COM]","described","_ole_iolelink","com.iolelink","oleidl/IOleLink"]
old-location: com\iolelink.htm
tech.root: com
ms.assetid: 4a34a90d-df1b-4bbf-8365-9d741c18ff74
ms.date: 12/05/2018
ms.keywords: IOleLink, IOleLink interface [COM], IOleLink interface [COM],described, _ole_iolelink, com.iolelink, oleidl/IOleLink
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleLink
 - oleidl/IOleLink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleLink
---

# IOleLink interface


## -description

Enables a linked object to provide its container with functions pertaining to linking. The most important of these functions is binding to the link source, that is, activating the connection to the document that stores the linked object's native data. <b>IOleLink</b> also defines functions for managing information about the linked object, such as the location of the link source and the cached presentation data for the linked object.

A container application can distinguish between embedded objects and linked objects by querying for <b>IOleLink</b>; only linked objects implement <b>IOleLink</b>.

## -inheritance

The <b>IOleLink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOleLink</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuieditlinksa">OleUIEditLinks</a>
