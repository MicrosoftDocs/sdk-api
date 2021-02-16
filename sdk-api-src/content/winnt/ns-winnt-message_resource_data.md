---
UID: NS:winnt._MESSAGE_RESOURCE_DATA
title: MESSAGE_RESOURCE_DATA (winnt.h)
description: Contains information about formatted text for display as an error message or in a message box in a message table resource.
helpviewer_keywords: ["*PMESSAGE_RESOURCE_DATA","MESSAGE_RESOURCE_DATA","MESSAGE_RESOURCE_DATA structure [Menus and Other Resources]","PMESSAGE_RESOURCE_DATA","PMESSAGE_RESOURCE_DATA structure pointer [Menus and Other Resources]","_win32_MESSAGE_RESOURCE_DATA_str","_win32_message_resource_data_str_cpp","menurc.message_resource_data","winnt/MESSAGE_RESOURCE_DATA","winnt/PMESSAGE_RESOURCE_DATA","winui._win32_message_resource_data_str"]
old-location: menurc\message_resource_data.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcestructures\message_resource_data.htm
ms.date: 12/05/2018
ms.keywords: '*PMESSAGE_RESOURCE_DATA, MESSAGE_RESOURCE_DATA, MESSAGE_RESOURCE_DATA structure [Menus and Other Resources], PMESSAGE_RESOURCE_DATA, PMESSAGE_RESOURCE_DATA structure pointer [Menus and Other Resources], _win32_MESSAGE_RESOURCE_DATA_str, _win32_message_resource_data_str_cpp, menurc.message_resource_data, winnt/MESSAGE_RESOURCE_DATA, winnt/PMESSAGE_RESOURCE_DATA, winui._win32_message_resource_data_str'
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
req.typenames: MESSAGE_RESOURCE_DATA, *PMESSAGE_RESOURCE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MESSAGE_RESOURCE_DATA
 - winnt/_MESSAGE_RESOURCE_DATA
 - PMESSAGE_RESOURCE_DATA
 - winnt/PMESSAGE_RESOURCE_DATA
 - MESSAGE_RESOURCE_DATA
 - winnt/MESSAGE_RESOURCE_DATA
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
 - MESSAGE_RESOURCE_DATA
---

# MESSAGE_RESOURCE_DATA structure


## -description

Contains information about formatted text for display as an error message or in a message box in a message table resource.

## -struct-fields

### -field NumberOfBlocks

Type: <b>DWORD</b>

The number of <a href="/windows/desktop/api/winnt/ns-winnt-message_resource_block">MESSAGE_RESOURCE_BLOCK</a> structures.

### -field Blocks

Type: <b><a href="/windows/desktop/api/winnt/ns-winnt-message_resource_block">MESSAGE_RESOURCE_BLOCK</a>[1]</b>

An array of structures. The array is the size indicated by the 
					<b>NumberOfBlocks</b>  member.

## -remarks

A <b>MESSAGE_RESOURCE_DATA</b> structure can contain one or more 
				<a href="/windows/desktop/api/winnt/ns-winnt-message_resource_block">MESSAGE_RESOURCE_BLOCK</a> structures, which can each contain one or more <a href="/windows/desktop/api/winnt/ns-winnt-message_resource_entry">MESSAGE_RESOURCE_ENTRY</a> structures.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winnt/ns-winnt-message_resource_block">MESSAGE_RESOURCE_BLOCK</a>



<a href="/windows/desktop/api/winnt/ns-winnt-message_resource_entry">MESSAGE_RESOURCE_ENTRY</a>



<b>Reference</b>



<a href="/windows/desktop/menurc/resources">Resources</a>