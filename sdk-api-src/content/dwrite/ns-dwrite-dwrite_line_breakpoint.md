---
UID: NS:dwrite.DWRITE_LINE_BREAKPOINT
title: DWRITE_LINE_BREAKPOINT
author: windows-sdk-content
description: Line breakpoint characteristics of a character.
old-location: directwrite\dwrite_line_breakpoint.htm
old-project: DirectWrite
ms.assetid: 6f2b26e9-95b3-4ac5-ba8e-7055f873d1da
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: DWRITE_LINE_BREAKPOINT, DWRITE_LINE_BREAKPOINT structure [Direct Write], directwrite.dwrite_line_breakpoint, dwrite/DWRITE_LINE_BREAKPOINT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dwrite.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_LINE_BREAKPOINT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DWRITE_LINE_BREAKPOINT structure


## -description


Line breakpoint characteristics of a character.


## -struct-fields




### -field breakConditionBefore

Type: <b>UINT8</b>

Indicates a breaking condition before the character.


### -field breakConditionAfter

Type: <b>UINT8</b>

Indicates a breaking condition after the character.


### -field isWhitespace

Type: <b>UINT8</b>

Indicates that the character is some form of whitespace, which may be meaningful for justification.


### -field isSoftHyphen

Type: <b>UINT8</b>

Indicates that the character is a soft hyphen, often used to indicate hyphenation points inside words.


### -field padding

Type: <b>UINT8</b>

Reserved for future use.

