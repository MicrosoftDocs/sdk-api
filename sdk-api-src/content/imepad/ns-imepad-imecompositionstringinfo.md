---
UID: NS:imepad.tagIMECOMPOSITIONSTRINGINFO
title: IMECOMPOSITIONSTRINGINFO (imepad.h)
description: Contains information of IME's composition string in an app.
helpviewer_keywords: ["*LPIMECOMPOSITIONSTRINGINFO","IMECOMPOSITIONSTRINGINFO","IMECOMPOSITIONSTRINGINFO structure [Internationalization for Windows Applications]","PIMECOMPOSITIONSTRINGINFO","PIMECOMPOSITIONSTRINGINFO structure pointer [Internationalization for Windows Applications]","imepad/IMECOMPOSITIONSTRINGINFO","imepad/PIMECOMPOSITIONSTRINGINFO","intl.imecompositionstringinfo"]
old-location: intl\imecompositionstringinfo.htm
tech.root: Intl
ms.assetid: 27124683-C4F9-4FF9-9004-9FF5B2B8B421
ms.date: 12/05/2018
ms.keywords: '*LPIMECOMPOSITIONSTRINGINFO, IMECOMPOSITIONSTRINGINFO, IMECOMPOSITIONSTRINGINFO structure [Internationalization for Windows Applications], PIMECOMPOSITIONSTRINGINFO, PIMECOMPOSITIONSTRINGINFO structure pointer [Internationalization for Windows Applications], imepad/IMECOMPOSITIONSTRINGINFO, imepad/PIMECOMPOSITIONSTRINGINFO, intl.imecompositionstringinfo'
req.header: imepad.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: IMECOMPOSITIONSTRINGINFO, *LPIMECOMPOSITIONSTRINGINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagIMECOMPOSITIONSTRINGINFO
 - imepad/tagIMECOMPOSITIONSTRINGINFO
 - LPIMECOMPOSITIONSTRINGINFO
 - imepad/LPIMECOMPOSITIONSTRINGINFO
 - IMECOMPOSITIONSTRINGINFO
 - imepad/IMECOMPOSITIONSTRINGINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Imepad.h
api_name:
 - IMECOMPOSITIONSTRINGINFO
---

# IMECOMPOSITIONSTRINGINFO structure


## -description

Contains information of IME's composition string in an app.

## -struct-fields

### -field iCompStrLen

Length (number of <b>WCHAR</b>s) of composition string.

### -field iCaretPos

Caret position of composition string.

### -field iEditStart

Position of composition string that is editable.

### -field iEditLen

Length of composition string that is editable.

### -field iTargetStart

Start position of target phrase of composition string.

### -field iTargetLen

Target phrase length of composition string.

## -see-also

<a href="/windows/desktop/api/imepad/nf-imepad-iimepad-request">IImePad::Request</a>