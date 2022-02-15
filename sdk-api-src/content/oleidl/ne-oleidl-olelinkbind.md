---
UID: NE:oleidl.tagOLELINKBIND
title: OLELINKBIND (oleidl.h)
description: Controls binding operations to a link source.
helpviewer_keywords: ["OLELINKBIND","OLELINKBIND enumeration [COM]","OLELINKBIND_EVENIFCLASSDIFF","_ole_OLELINKBIND","com.olelinkbind","oleidl/OLELINKBIND","oleidl/OLELINKBIND_EVENIFCLASSDIFF"]
old-location: com\olelinkbind.htm
tech.root: com
ms.assetid: a5b8bb64-002f-4c85-b6bb-61b2fba88c0f
ms.date: 12/05/2018
ms.keywords: OLELINKBIND, OLELINKBIND enumeration [COM], OLELINKBIND_EVENIFCLASSDIFF, _ole_OLELINKBIND, com.olelinkbind, oleidl/OLELINKBIND, oleidl/OLELINKBIND_EVENIFCLASSDIFF
req.header: oleidl.h
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
req.typenames: OLELINKBIND
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOLELINKBIND
 - oleidl/tagOLELINKBIND
 - OLELINKBIND
 - oleidl/OLELINKBIND
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OleIdl.h
api_name:
 - OLELINKBIND
---

# OLELINKBIND enumeration


## -description

Controls binding operations to a link source.

## -enum-fields

### -field OLELINKBIND_EVENIFCLASSDIFF:1

The binding operation should proceed even if the current class of the link source is different from the last time the link was bound. For example, the link source could be a Lotus spreadsheet that was converted to an Excel spreadsheet.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-bindtosource">IOleLink::BindToSource</a>
