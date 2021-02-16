---
UID: NS:docobj._tagOLECMDTEXT
title: OLECMDTEXT (docobj.h)
description: Specifies a text name or status string for a single command identifier.
helpviewer_keywords: ["OLECMDTEXT","OLECMDTEXT structure [COM]","_ole_OLECMDTEXT","com.olecmdtext","docobj/OLECMDTEXT"]
old-location: com\olecmdtext.htm
tech.root: com
ms.assetid: c9552d2a-fb51-4d9f-acd5-32b3f20a9e1e
ms.date: 12/05/2018
ms.keywords: OLECMDTEXT, OLECMDTEXT structure [COM], _ole_OLECMDTEXT, com.olecmdtext, docobj/OLECMDTEXT
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
req.typenames: OLECMDTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagOLECMDTEXT
 - docobj/_tagOLECMDTEXT
 - OLECMDTEXT
 - docobj/OLECMDTEXT
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
 - OLECMDTEXT
---

# OLECMDTEXT structure


## -description

Specifies a text name or status string for a single command identifier.

## -struct-fields

### -field cmdtextf

A value from the <a href="/windows/desktop/api/docobj/ne-docobj-olecmdtextf">OLECMDTEXTF</a> enumeration describing whether the <b>rgwz</b> member contains a command name or status text.

### -field cwActual

The number of characters actually written into the <b>rgwz</b> buffer before <a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-querystatus">IOleCommandTarget::QueryStatus</a> returns.

### -field cwBuf

The number of elements in the <b>rgwz</b> array.

### -field rgwz

A caller-allocated array of wide characters to receive the command name or status text.

## -see-also

<a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-querystatus">IOleCommandTarget::QueryStatus</a>



<a href="/windows/desktop/api/docobj/ne-docobj-olecmdtextf">OLECMDTEXTF</a>