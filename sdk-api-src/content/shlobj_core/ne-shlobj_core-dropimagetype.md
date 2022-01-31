---
UID: NE:shlobj_core.__unnamed_enum_6
title: DROPIMAGETYPE (shlobj_core.h)
description: Values used with the DROPDESCRIPTION structure to specify the drop image.
helpviewer_keywords: ["DROPIMAGETYPE","DROPIMAGETYPE enumeration [Windows Shell]","DROPIMAGE_COPY","DROPIMAGE_INVALID","DROPIMAGE_LABEL","DROPIMAGE_LINK","DROPIMAGE_MOVE","DROPIMAGE_NOIMAGE","DROPIMAGE_NONE","DROPIMAGE_WARNING","_shell_DROPIMAGETYPE","shell.DROPIMAGETYPE","shlobj_core/DROPIMAGETYPE","shlobj_core/DROPIMAGE_COPY","shlobj_core/DROPIMAGE_INVALID","shlobj_core/DROPIMAGE_LABEL","shlobj_core/DROPIMAGE_LINK","shlobj_core/DROPIMAGE_MOVE","shlobj_core/DROPIMAGE_NOIMAGE","shlobj_core/DROPIMAGE_NONE","shlobj_core/DROPIMAGE_WARNING"]
old-location: shell\DROPIMAGETYPE.htm
tech.root: shell
ms.assetid: eeaf8bd4-25ab-4ec3-9da9-9a72ba3813b9
ms.date: 12/05/2018
ms.keywords: DROPIMAGETYPE, DROPIMAGETYPE enumeration [Windows Shell], DROPIMAGE_COPY, DROPIMAGE_INVALID, DROPIMAGE_LABEL, DROPIMAGE_LINK, DROPIMAGE_MOVE, DROPIMAGE_NOIMAGE, DROPIMAGE_NONE, DROPIMAGE_WARNING, _shell_DROPIMAGETYPE, shell.DROPIMAGETYPE, shlobj_core/DROPIMAGETYPE, shlobj_core/DROPIMAGE_COPY, shlobj_core/DROPIMAGE_INVALID, shlobj_core/DROPIMAGE_LABEL, shlobj_core/DROPIMAGE_LINK, shlobj_core/DROPIMAGE_MOVE, shlobj_core/DROPIMAGE_NOIMAGE, shlobj_core/DROPIMAGE_NONE, shlobj_core/DROPIMAGE_WARNING
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows 7 [desktop apps only]
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
req.typenames: DROPIMAGETYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DROPIMAGETYPE
 - shlobj_core/DROPIMAGETYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - DROPIMAGETYPE
---

# DROPIMAGETYPE enumeration


## -description

Values used with the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription">DROPDESCRIPTION</a> structure to specify the drop image.

## -enum-fields

### -field DROPIMAGE_INVALID:-1

No drop image preference; use the default image.

### -field DROPIMAGE_NONE:0

A red bisected circle such as that found on a "no smoking" sign.

### -field DROPIMAGE_COPY

A plus sign (+) that indicates a copy operation.

### -field DROPIMAGE_MOVE

An arrow that indicates a move operation.

### -field DROPIMAGE_LINK

An arrow that indicates a link.

### -field DROPIMAGE_LABEL:6

A tag icon that indicates that the metadata will be changed.

### -field DROPIMAGE_WARNING:7

A yellow exclamation mark that indicates that a problem has been encountered in the operation.

### -field DROPIMAGE_NOIMAGE:8

<b>Windows 7 and later</b>. Use no drop image.
