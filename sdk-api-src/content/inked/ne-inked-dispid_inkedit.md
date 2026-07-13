---
UID: NE:inked.DISPID_InkEdit
tech.root: tablet
title: DISPID_InkEdit
ms.date: 02/07/2023
targetos: Windows
description: Specifies various ink editor states.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: inked.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.target-type: Windows
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - inked.h
api_name:
 - DISPID_InkEdit
f1_keywords:
 - DISPID_InkEdit
 - inked/DISPID_InkEdit
dev_langs:
 - c++
helpviewer_keywords:
 - DISPID_InkEdit
---

# DISPID_InkEdit enumeration

## -description

Specifies various ink editor states.

## -enum-fields

### -field DISPID_Text

Text.

### -field DISPID_TextRTF

Text, including all RTF (Rich Text Format) codes.

### -field DISPID_Hwnd

Handle.

### -field DISPID_DisableNoScroll

Scroll disabled.

### -field DISPID_Locked

Locked.

### -field DISPID_Enabled

Enabled.

### -field DISPID_MaxLength

Maximum number of characters an InkEdit control can hold.

### -field DISPID_MultiLine

Multiline.

### -field DISPID_ScrollBars

Scroll bars.

### -field DISPID_RTSelStart

Starting point of the selected text.

### -field DISPID_RTSelLength

Selected text length.

### -field DISPID_RTSelText

Selected text.

### -field DISPID_SelAlignment

Selected text alignment.

### -field DISPID_SelBold

Selected text bold.

### -field DISPID_SelCharOffset

Selected text appears on the baseline (normal), as a superscript above the baseline, or as a subscript below the baseline.

### -field DISPID_SelColor

Text selection highlight color.

### -field DISPID_SelFontName

Text selection font name.

### -field DISPID_SelFontSize

Text selection font size.

### -field DISPID_SelItalic

Text selection italicized.

### -field DISPID_SelRTF

Text selection is RTF.

### -field DISPID_SelUnderline

Text selection underlined.

### -field DISPID_DragIcon

Drag icon.

### -field DISPID_Status

Status.

### -field DISPID_UseMouseForInput

Mouse inking.

### -field DISPID_InkMode

Ink collection is disabled, ink is collected, or ink and gestures are collected.

### -field DISPID_InkInsertMode

Ink is inserted as either text or ink.

### -field DISPID_RecoTimeout

Length of time, in milliseconds, between the last IInkStrokeDisp object collected and the beginning of text recognition.

### -field DISPID_DrawAttr

Ink drawing attributes.

### -field DISPID_Recognizer

Recognizer enabled.

### -field DISPID_Factoid

[Factoid](/windows/win32/tablet/factoid-constants) constant used to constrain recognition results.

### -field DISPID_SelInk

Ink selection.

### -field DISPID_SelInksDisplayMode

Text selection displayed as ink or text.

### -field DISPID_Recognize

Recognition active.

### -field DISPID_GetGestStatus

Getting gesture recognition status.

### -field DISPID_SetGestStatus

Setting gesture recognition status.

### -field DISPID_Refresh

Redraw.

## -remarks

## -see-also

[IInkEdit interface](nn-inked-iinkedit.md)
