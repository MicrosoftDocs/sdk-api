---
UID: NS:uxtheme._MARGINS
title: MARGINS (uxtheme.h)
description: Returned by the GetThemeMargins function to define the margins of windows that have visual styles applied.
helpviewer_keywords: ["*PMARGINS","MARGINS","MARGINS structure [Windows Controls]","PMARGINS","PMARGINS structure pointer [Windows Controls]","controls.MARGINS","controls.inet_MARGINS","inet_MARGINS","inet_MARGINS_cpp","uxtheme/MARGINS","uxtheme/PMARGINS"]
old-location: controls\MARGINS.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\structures\margins.htm
ms.date: 12/05/2018
ms.keywords: '*PMARGINS, MARGINS, MARGINS structure [Windows Controls], PMARGINS, PMARGINS structure pointer [Windows Controls], controls.MARGINS, controls.inet_MARGINS, inet_MARGINS, inet_MARGINS_cpp, uxtheme/MARGINS, uxtheme/PMARGINS'
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: MARGINS, *PMARGINS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MARGINS
 - uxtheme/_MARGINS
 - PMARGINS
 - uxtheme/PMARGINS
 - MARGINS
 - uxtheme/MARGINS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uxtheme.h
api_name:
 - MARGINS
---

# MARGINS structure


## -description

Returned by the <a href="/windows/desktop/api/uxtheme/nf-uxtheme-getthememargins">GetThemeMargins</a> function to define the margins of windows that have visual styles applied.

## -struct-fields

### -field cxLeftWidth

Type: <b>int</b>

Width of the left border that retains its size.

### -field cxRightWidth

Type: <b>int</b>

Width of the right border that retains its size.

### -field cyTopHeight

Type: <b>int</b>

Height of the top border that retains its size.

### -field cyBottomHeight

Type: <b>int</b>

Height of the bottom border that retains its size.

## -see-also

<a href="/windows/desktop/api/uxtheme/nf-uxtheme-getthememargins">GetThemeMargins</a>