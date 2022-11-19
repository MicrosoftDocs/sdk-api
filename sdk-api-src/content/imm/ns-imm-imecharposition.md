---
UID: NS:imm.tagIMECHARPOSITION
title: IMECHARPOSITION (imm.h)
description: The IMECHARPOSITION (imm.h) structure contains information about the character position in the composition window.
helpviewer_keywords: ["*LPIMECHARPOSITION","*NPIMECHARPOSITION","*PIMECHARPOSITION","IMECHARPOSITION","IMECHARPOSITION structure [Internationalization for Windows Applications]","PIMECHARPOSITION","PIMECHARPOSITION structure pointer [Internationalization for Windows Applications]","_win32_IMECHARPOSITION_str","imm/IMECHARPOSITION","imm/PIMECHARPOSITION","intl.imecharposition","tagIMECHARPOSITION"]
old-location: intl\imecharposition.htm
tech.root: Intl
ms.assetid: 5c278df0-ce90-4f9d-915e-45dadc823360
ms.date: 08/04/2022
ms.keywords: '*LPIMECHARPOSITION, *NPIMECHARPOSITION, *PIMECHARPOSITION, IMECHARPOSITION, IMECHARPOSITION structure [Internationalization for Windows Applications], PIMECHARPOSITION, PIMECHARPOSITION structure pointer [Internationalization for Windows Applications], _win32_IMECHARPOSITION_str, imm/IMECHARPOSITION, imm/PIMECHARPOSITION, intl.imecharposition, tagIMECHARPOSITION'
req.header: imm.h
req.include-header: Immdev.h, Windows.h
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
req.typenames: IMECHARPOSITION, *PIMECHARPOSITION, *NPIMECHARPOSITION, *LPIMECHARPOSITION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagIMECHARPOSITION
 - imm/tagIMECHARPOSITION
 - PIMECHARPOSITION
 - imm/PIMECHARPOSITION
 - IMECHARPOSITION
 - imm/IMECHARPOSITION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Imm.h
api_name:
 - IMECHARPOSITION
---

# IMECHARPOSITION structure


## -description

Contains information about the character position in the composition window.

## -struct-fields

### -field dwSize

Size of the structure, in bytes.

### -field dwCharPos

Character offset in the composition string, in <b>TCHAR</b> values.

### -field pt

A <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure containing the coordinate of the top left point of requested character in screen coordinates. The top left point is based on the character baseline in any text flow.

### -field cLineHeight

Height of a line that contains the requested character, in pixels.

### -field rcDocument

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure containing the editable area for text, in screen coordinates, for the application.

## -remarks

When an application uses IME to draw the composition string, the members of this structure are automatically filled. Applications that draw the composition string themselves, rather than relying on the IME, are responsible for filling all the fields defined in the structure.

## -see-also

<a href="/windows/desktop/Intl/imr-querycharposition">IMR_QUERYCHARPOSITION</a>



<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-structures">Input Method Manager Structures</a>
