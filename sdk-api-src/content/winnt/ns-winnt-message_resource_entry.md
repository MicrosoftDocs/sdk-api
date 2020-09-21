---
UID: NS:winnt._MESSAGE_RESOURCE_ENTRY
title: MESSAGE_RESOURCE_ENTRY (winnt.h)
description: Contains the error message or message box display text for a message table resource.
helpviewer_keywords: ["*PMESSAGE_RESOURCE_ENTRY","MESSAGE_RESOURCE_ENTRY","MESSAGE_RESOURCE_ENTRY structure [Menus and Other Resources]","PMESSAGE_RESOURCE_ENTRY","PMESSAGE_RESOURCE_ENTRY structure pointer [Menus and Other Resources]","_win32_MESSAGE_RESOURCE_ENTRY_str","_win32_message_resource_entry_str_cpp","menurc.message_resource_entry","winnt/MESSAGE_RESOURCE_ENTRY","winnt/PMESSAGE_RESOURCE_ENTRY","winui._win32_message_resource_entry_str"]
old-location: menurc\message_resource_entry.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcestructures\message_resource_entry.htm
ms.date: 12/05/2018
ms.keywords: '*PMESSAGE_RESOURCE_ENTRY, MESSAGE_RESOURCE_ENTRY, MESSAGE_RESOURCE_ENTRY structure [Menus and Other Resources], PMESSAGE_RESOURCE_ENTRY, PMESSAGE_RESOURCE_ENTRY structure pointer [Menus and Other Resources], _win32_MESSAGE_RESOURCE_ENTRY_str, _win32_message_resource_entry_str_cpp, menurc.message_resource_entry, winnt/MESSAGE_RESOURCE_ENTRY, winnt/PMESSAGE_RESOURCE_ENTRY, winui._win32_message_resource_entry_str'
req.header: winnt.h
req.include-header: Windows.h
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
req.typenames: MESSAGE_RESOURCE_ENTRY, *PMESSAGE_RESOURCE_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MESSAGE_RESOURCE_ENTRY
 - winnt/_MESSAGE_RESOURCE_ENTRY
 - PMESSAGE_RESOURCE_ENTRY
 - winnt/PMESSAGE_RESOURCE_ENTRY
 - MESSAGE_RESOURCE_ENTRY
 - winnt/MESSAGE_RESOURCE_ENTRY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - MESSAGE_RESOURCE_ENTRY
---

# MESSAGE_RESOURCE_ENTRY structure


## -description

Contains the error message or message box display text for a message table resource.

## -struct-fields

### -field Length

Type: <b>WORD</b>

The length, in bytes, of the <b>MESSAGE_RESOURCE_ENTRY</b> structure.

### -field Flags

Type: <b>WORD</b>

Indicates that the string is encoded in Unicode, if equal to the value 0x0001. Indicates that the string is encoded in ANSI, if equal to the value 0x0000.

### -field Text

Type: <b>BYTE[1]</b>

Pointer to an array that contains the error message or message box display text.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winnt/ns-winnt-message_resource_block">MESSAGE_RESOURCE_BLOCK</a>



<a href="/windows/desktop/api/winnt/ns-winnt-message_resource_data">MESSAGE_RESOURCE_DATA</a>



<b>Reference</b>



<a href="/windows/desktop/menurc/resources">Resources</a>