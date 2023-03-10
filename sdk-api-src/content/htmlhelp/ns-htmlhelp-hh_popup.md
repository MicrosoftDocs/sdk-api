---
UID: NS:htmlhelp.tagHH_POPUP
title: HH_POPUP (htmlhelp.h)
description: Use this structure to specify or modify the attributes of a pop-up window.
helpviewer_keywords: ["HH_POPUP","HH_POPUP structure [HTML Help Workshop]","htmlhelp.hh_popup_structure","htmlhelp/HH_POPUP","vsconStrhhpopup"]
old-location: htmlhelp\hh_popup_structure.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\vsconstrhhpopup.htm
ms.date: 12/05/2018
ms.keywords: HH_POPUP, HH_POPUP structure [HTML Help Workshop], htmlhelp.hh_popup_structure, htmlhelp/HH_POPUP, vsconStrhhpopup
req.header: htmlhelp.h
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
req.typenames: HH_POPUP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagHH_POPUP
 - htmlhelp/tagHH_POPUP
 - HH_POPUP
 - htmlhelp/HH_POPUP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - HtmlHelp.h
api_name:
 - HH_POPUP
---

# HH_POPUP structure


## -description

Use this structure to specify or modify the attributes of a pop-up window.

## -struct-fields

### -field cbStruct

Specifies the size of the structure. This value must always be filled in before passing the structure to HtmlHelp().

### -field hinst

Instance handle of the program or DLL to retrieve the string resource from. Ignored if <i>idString</i> is zero, or if <i>idString</i> specifies a file name.

### -field idString

Specifies zero, a resource ID, or a topic number in a text file.

### -field pszText

Specifies the text to display if <i>idString</i> is zero.

### -field pt

Specifies (in pixels) where the top center of the pop-up window should be located.

### -field clrForeground

Specifies the RGB value to use for the foreground color of the pop-up window. To use the system color for the window text, specify -1.

### -field clrBackground

Specifies the RGB value to use for the background color of the pop-up window. To use the system color for the window background, specify -1.

### -field rcMargins

Specifies (in pixels) the margins to use on the left, top, right, and bottom sides of the pop-up window. The default for all rectangle members is -1.

### -field pszFont

Specifies the font attributes to use for the text in the pop-up window.


Use the following format to specify font family, point size, character set, and font format:

facename[, point size[, charset[ BOLD ITALIC UNDERLINE]]]

To omit an attribute, enter a comma. For example, to specify bold, 10-pt, MS Sans Serif font, <i>pszFont</i> would be:

MS Sans Serif, 10, , BOLD

## -see-also

<a href="/previous-versions/windows/desktop/htmlhelp/about-structures">About Structures</a>