---
UID: NS:peerdist.peerdist_content_tag_tag
title: PEERDIST_CONTENT_TAG (peerdist.h)
description: PEERDIST_CONTENT_TAG structure contains a client supplied content tag as an input to the PeerDistClientOpenContent API.
helpviewer_keywords: ["*PPEERDIST_CONTENT_TAG","PEERDIST_CONTENT_TAG","PEERDIST_CONTENT_TAG structure [Peer Networking]","PPEERDIST_CONTENT_TAG","PPEERDIST_CONTENT_TAG structure pointer [Peer Networking]","p2p.peerdist_content_tag","peerdist/PEERDIST_CONTENT_TAG","peerdist/PPEERDIST_CONTENT_TAG"]
old-location: p2p\peerdist_content_tag.htm
tech.root: p2p
ms.assetid: 09eab22b-0534-44db-9954-ff5a9c5667f9
ms.date: 12/05/2018
ms.keywords: '*PPEERDIST_CONTENT_TAG, PEERDIST_CONTENT_TAG, PEERDIST_CONTENT_TAG structure [Peer Networking], PPEERDIST_CONTENT_TAG, PPEERDIST_CONTENT_TAG structure pointer [Peer Networking], p2p.peerdist_content_tag, peerdist/PEERDIST_CONTENT_TAG, peerdist/PPEERDIST_CONTENT_TAG'
req.header: peerdist.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
targetos: Windows
req.typenames: PEERDIST_CONTENT_TAG, *PPEERDIST_CONTENT_TAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peerdist_content_tag_tag
 - peerdist/peerdist_content_tag_tag
 - PPEERDIST_CONTENT_TAG
 - peerdist/PPEERDIST_CONTENT_TAG
 - PEERDIST_CONTENT_TAG
 - peerdist/PEERDIST_CONTENT_TAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - peerdist.h
api_name:
 - PEERDIST_CONTENT_TAG
---

# PEERDIST_CONTENT_TAG structure


## -description

The <b>PEERDIST_CONTENT_TAG</b> structure contains a client supplied content tag as an input to the <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientopencontent">PeerDistClientOpenContent</a> API.

## -struct-fields

### -field Data

A 16 byte tag associated with the open content.

## -see-also

<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientflushcontent">PeerDistClientFlushContent</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientopencontent">PeerDistClientOpenContent</a>