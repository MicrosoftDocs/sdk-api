---
UID: NE:uiautomationcore.CaretPosition
title: CaretPosition (uiautomationcore.h)
description: Contains possible values for the CaretPosition text attribute, which indicates the location of the caret relative to a line of text in a text range.
helpviewer_keywords: ["CaretPosition","CaretPosition enumeration [Windows Accessibility]","CaretPosition_BeginningOfLine","CaretPosition_EndOfLine","CaretPosition_Unknown","uiautomationcore/CaretPosition","uiautomationcore/CaretPosition_BeginningOfLine","uiautomationcore/CaretPosition_EndOfLine","uiautomationcore/CaretPosition_Unknown","winauto.uiauto_CaretPosition"]
old-location: winauto\uiauto_CaretPosition.htm
tech.root: WinAuto
ms.assetid: 9284DCBB-FC6A-4895-8AE6-58C47BB3A047
ms.date: 12/05/2018
ms.keywords: CaretPosition, CaretPosition enumeration [Windows Accessibility], CaretPosition_BeginningOfLine, CaretPosition_EndOfLine, CaretPosition_Unknown, uiautomationcore/CaretPosition, uiautomationcore/CaretPosition_BeginningOfLine, uiautomationcore/CaretPosition_EndOfLine, uiautomationcore/CaretPosition_Unknown, winauto.uiauto_CaretPosition
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CaretPosition
 - uiautomationcore/CaretPosition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationCore.h
api_name:
 - CaretPosition
---

# CaretPosition enumeration


## -description

Contains possible values for the <a href="/windows/desktop/WinAuto/uiauto-textattribute-ids">CaretPosition</a> text attribute, which indicates the location of the caret relative to a line of text in a text range.

## -enum-fields

### -field CaretPosition_Unknown:0

The caret is not at the beginning or the end of a line.

### -field CaretPosition_EndOfLine:1

The caret is at the end of a line.

### -field CaretPosition_BeginningOfLine:2

The caret is at the beginning of a line.

## -remarks

The provider of a text-based control considers the caret to be at some character position in the text. For example, if the caret is at the start of the text, it lies at position 0. If the caret is just after the first character, it lies at position 1, and so on. When text wraps around at the end of a line, typically a space is shown at the end of the line, and a non-space character at the start of the next line. The user might be able to place the caret after the space at the end of the first line, or before the non-space character at the start of the next line. However, both places are considered to be the same character position. The <a href="/windows/desktop/WinAuto/uiauto-textattribute-ids">CaretPosition</a> attribute indicates whether the caret is shown at the end or the beginning of a line. If the caret lies at neither of these positions, the <b>CaretPosition</b> attribute is <b>CaretPosition_Unknown</b>.
