---
UID: NE:docobj.OLECMDTEXTF
title: OLECMDTEXTF (docobj.h)
description: Specifies the type of information that an object should store in the OLECMDTEXT structure passed in IOleCommandTarget::QueryStatus.
helpviewer_keywords: ["OLECMDTEXTF","OLECMDTEXTF enumeration [COM]","OLECMDTEXTF_NAME","OLECMDTEXTF_NONE","OLECMDTEXTF_STATUS","_ole_OLECMDTEXTF","com.olecmdtextf","docobj/OLECMDTEXTF","docobj/OLECMDTEXTF_NAME","docobj/OLECMDTEXTF_NONE","docobj/OLECMDTEXTF_STATUS"]
old-location: com\olecmdtextf.htm
tech.root: com
ms.assetid: 8978331a-33b6-4f57-b5a3-aae305c1d872
ms.date: 12/05/2018
ms.keywords: OLECMDTEXTF, OLECMDTEXTF enumeration [COM], OLECMDTEXTF_NAME, OLECMDTEXTF_NONE, OLECMDTEXTF_STATUS, _ole_OLECMDTEXTF, com.olecmdtextf, docobj/OLECMDTEXTF, docobj/OLECMDTEXTF_NAME, docobj/OLECMDTEXTF_NONE, docobj/OLECMDTEXTF_STATUS
req.header: docobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: OLECMDTEXTF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OLECMDTEXTF
 - docobj/OLECMDTEXTF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DocObj.h
api_name:
 - OLECMDTEXTF
---

# OLECMDTEXTF enumeration


## -description

Specifies the type of information that an object should store in the <a href="/windows/desktop/api/docobj/ns-docobj-olecmdtext">OLECMDTEXT</a> structure passed in <a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-querystatus">IOleCommandTarget::QueryStatus</a>. One value from this enumeration is stored the <b>cmdtextf</b> member of the <b>OLECMDTEXT</b> structure to indicate the desired information.

## -enum-fields

### -field OLECMDTEXTF_NONE:0

No extra information is requested.

### -field OLECMDTEXTF_NAME:1

The object should provide the localized name of the command.

### -field OLECMDTEXTF_STATUS:2

The object should provide a localized status string for the command.

## -see-also

<a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-querystatus">IOleCommandTarget::QueryStatus</a>



<a href="/windows/desktop/api/docobj/ns-docobj-olecmdtext">OLECMDTEXT</a>
