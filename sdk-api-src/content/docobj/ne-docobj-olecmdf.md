---
UID: NE:docobj.OLECMDF
title: OLECMDF (docobj.h)
description: Specifies the type of support provided by an object for the command specified in an OLECMD structure.
helpviewer_keywords: ["OLECMDF","OLECMDF enumeration [COM]","OLECMDF_DEFHIDEONCTXTMENU","OLECMDF_ENABLED","OLECMDF_INVISIBLE","OLECMDF_LATCHED","OLECMDF_NINCHED","OLECMDF_SUPPORTED","_ole_OLECMDF","com.olecmdf","docobj/OLECMDF","docobj/OLECMDF_DEFHIDEONCTXTMENU","docobj/OLECMDF_ENABLED","docobj/OLECMDF_INVISIBLE","docobj/OLECMDF_LATCHED","docobj/OLECMDF_NINCHED","docobj/OLECMDF_SUPPORTED"]
old-location: com\olecmdf.htm
tech.root: com
ms.assetid: feb493da-0db2-4251-ba6f-ded1fbd3e430
ms.date: 12/05/2018
ms.keywords: OLECMDF, OLECMDF enumeration [COM], OLECMDF_DEFHIDEONCTXTMENU, OLECMDF_ENABLED, OLECMDF_INVISIBLE, OLECMDF_LATCHED, OLECMDF_NINCHED, OLECMDF_SUPPORTED, _ole_OLECMDF, com.olecmdf, docobj/OLECMDF, docobj/OLECMDF_DEFHIDEONCTXTMENU, docobj/OLECMDF_ENABLED, docobj/OLECMDF_INVISIBLE, docobj/OLECMDF_LATCHED, docobj/OLECMDF_NINCHED, docobj/OLECMDF_SUPPORTED
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
req.typenames: OLECMDF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OLECMDF
 - docobj/OLECMDF
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
 - OLECMDF
---

# OLECMDF enumeration


## -description

Specifies the type of support provided by an object for the command specified in an <a href="/windows/desktop/api/docobj/ns-docobj-olecmd">OLECMD</a> structure.

## -enum-fields

### -field OLECMDF_SUPPORTED:0x1

The command is supported by this object.

### -field OLECMDF_ENABLED:0x2

The command is available and enabled.

### -field OLECMDF_LATCHED:0x4

The command is an on-off toggle and is currently on.

### -field OLECMDF_NINCHED:0x8

Reserved for future use.

### -field OLECMDF_INVISIBLE:0x10

The command is hidden.

### -field OLECMDF_DEFHIDEONCTXTMENU:0x20

The command is hidden on the context menu.

## -remarks

Values from the <b>OLECMDF</b> enumeration are used to fill the value of the <b>cmdf</b> member of <a href="/windows/desktop/api/docobj/ns-docobj-olecmd">OLECMD</a> structures passed to <a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-querystatus">IOleCommandTarget::QueryStatus</a>.

## -see-also

<a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-querystatus">IOleCommandTarget::QueryStatus</a>



<a href="/windows/desktop/api/docobj/ns-docobj-olecmd">OLECMD</a>
