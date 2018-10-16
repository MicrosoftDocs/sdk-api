---
UID: NS:winnt._MESSAGE_RESOURCE_ENTRY
title: "_MESSAGE_RESOURCE_ENTRY"
author: windows-sdk-content
description: Contains the error message or message box display text for a message table resource.
old-location: menurc\message_resource_entry.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcestructures\message_resource_entry.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PMESSAGE_RESOURCE_ENTRY, MESSAGE_RESOURCE_ENTRY, MESSAGE_RESOURCE_ENTRY structure [Menus and Other Resources], PMESSAGE_RESOURCE_ENTRY, PMESSAGE_RESOURCE_ENTRY structure pointer [Menus and Other Resources], _MESSAGE_RESOURCE_ENTRY, _win32_MESSAGE_RESOURCE_ENTRY_str, _win32_message_resource_entry_str_cpp, menurc.message_resource_entry, winnt/MESSAGE_RESOURCE_ENTRY, winnt/PMESSAGE_RESOURCE_ENTRY, winui._win32_message_resource_entry_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - MESSAGE_RESOURCE_ENTRY
product: Windows
targetos: Windows
req.typenames: MESSAGE_RESOURCE_ENTRY, *PMESSAGE_RESOURCE_ENTRY
req.redist: 
---

# _MESSAGE_RESOURCE_ENTRY structure


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



<a href="https://msdn.microsoft.com/573f22be-d204-4c0d-9c45-bd6d46094e32">MESSAGE_RESOURCE_BLOCK</a>



<a href="https://msdn.microsoft.com/439cf64e-29be-49ab-8bbf-cb98ac2e41cd">MESSAGE_RESOURCE_DATA</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>
 

 

