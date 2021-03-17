---
UID: NS:winternl._STRING
title: STRING (winternl.h)
description: Used with the RtlUnicodeStringToOemString function.
helpviewer_keywords: ["*PSTRING","ANSI_STRING","OEM_STRING","OEM_STRING structure [Windows API]","PSTRING","PSTRING structure pointer [Windows API]","STRING","STRING structure [Windows API]","_STRING","_win32_STRING","winprog._win32_string","winternl/OEM_STRING","winternl/PSTRING","winternl/STRING","winui._win32_string"]
old-location: winprog\_win32_string.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\string.htm
ms.date: 12/05/2018
ms.keywords: '*PSTRING, ANSI_STRING, OEM_STRING, OEM_STRING structure [Windows API], PSTRING, PSTRING structure pointer [Windows API], STRING, STRING structure [Windows API], _STRING, _win32_STRING, winprog._win32_string, winternl/OEM_STRING, winternl/PSTRING, winternl/STRING, winui._win32_string'
req.header: winternl.h
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
req.typenames: STRING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _STRING
 - winternl/_STRING
 - STRING
 - winternl/STRING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winternl.h
api_name:
 - STRING
---

# STRING structure


## -description

Used with the <a href="/windows/desktop/api/winternl/nf-winternl-rtlunicodestringtooemstring">RtlUnicodeStringToOemString</a> function.

## -struct-fields

### -field Length

The length of the buffer.

### -field MaximumLength

The maximum length of the buffer.

### -field Buffer

The address of the buffer.

## -remarks

The data type used in the <b>DestinationString</b> parameter of the <a href="/windows/desktop/api/winternl/nf-winternl-rtlunicodestringtooemstring">RtlUnicodeStringToOemString</a> function, <code> POEM_STRING</code>, is defined as:
		
                

<code>typedef PSTRING POEM_STRING;</code>