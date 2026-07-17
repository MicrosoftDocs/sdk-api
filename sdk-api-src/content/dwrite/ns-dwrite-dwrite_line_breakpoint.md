---
UID: NS:dwrite.DWRITE_LINE_BREAKPOINT
title: DWRITE_LINE_BREAKPOINT (dwrite.h)
description: Line breakpoint characteristics of a character.
helpviewer_keywords: ["DWRITE_LINE_BREAKPOINT","DWRITE_LINE_BREAKPOINT structure [Direct Write]","directwrite.dwrite_line_breakpoint","dwrite/DWRITE_LINE_BREAKPOINT"]
old-location: directwrite\dwrite_line_breakpoint.htm
tech.root: DirectWrite
ms.assetid: 6f2b26e9-95b3-4ac5-ba8e-7055f873d1da
ms.date: 12/05/2018
ms.keywords: DWRITE_LINE_BREAKPOINT, DWRITE_LINE_BREAKPOINT structure [Direct Write], directwrite.dwrite_line_breakpoint, dwrite/DWRITE_LINE_BREAKPOINT
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - DWRITE_LINE_BREAKPOINT
 - dwrite/DWRITE_LINE_BREAKPOINT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_LINE_BREAKPOINT
---

# DWRITE_LINE_BREAKPOINT structure


## -description

Line breakpoint characteristics of a character.

## -struct-fields

### -field breakConditionBefore

Type: <b>UINT8 : 2</b>

Indicates a breaking condition before the character, equivalent to [DWRITE_BREAK_CONDITION](/windows/win32/api/dwrite/ne-dwrite-dwrite_break_condition).

### -field breakConditionAfter

Type: <b>UINT8 : 2</b>

Indicates a breaking condition after the character, equivalent to [DWRITE_BREAK_CONDITION](/windows/win32/api/dwrite/ne-dwrite-dwrite_break_condition).

### -field isWhitespace

Type: <b>UINT8 : 1</b>

Indicates that the character is some form of whitespace, which may be meaningful for justification.

### -field isSoftHyphen

Type: <b>UINT8 : 1</b>

Indicates that the character is a soft hyphen, often used to indicate hyphenation points inside words.

### -field padding

Type: <b>UINT8 : 2</b>

Reserved for future use.

## -see-also

[DWRITE_BREAK_CONDITION](/windows/win32/api/dwrite/ne-dwrite-dwrite_break_condition)
