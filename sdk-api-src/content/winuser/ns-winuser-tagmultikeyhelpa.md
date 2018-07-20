---
UID: NS:winuser.tagMULTIKEYHELPA
title: tagMULTIKEYHELPA
author: windows-sdk-content
description: Specifies a keyword to search for and the keyword table to be searched by Windows Help.
old-location: shell\MULTIKEYHELP_str.htm
old-project: shell
ms.assetid: 5fe0cd44-196c-4d9a-b9f8-2a97a92f2545
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "*LPMULTIKEYHELPA, *PMULTIKEYHELPA, MULTIKEYHELP, MULTIKEYHELP structure [Windows Shell], MULTIKEYHELPA, _win32_MULTIKEYHELP_str, shell.MULTIKEYHELP_str, tagMULTIKEYHELPA, tagMULTIKEYHELPW, winuser/MULTIKEYHELP"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
tech.root: 
req.typenames: MULTIKEYHELPA, *PMULTIKEYHELPA, *LPMULTIKEYHELPA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - MULTIKEYHELP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagMULTIKEYHELPA structure


## -description


Specifies a keyword to search for and the keyword table to be searched by Windows Help.


## -struct-fields




### -field mkSize

Type: <b>DWORD</b>

The structure size, in bytes.


### -field mkKeylist

Type: <b>TCHAR</b>

A single character that identifies the keyword table to search.


### -field szKeyphrase

Type: <b>TCHAR[1]</b>

A null-terminated text string that specifies the keyword to locate in the keyword table.


## -see-also




<a href="https://msdn.microsoft.com/fce80bac-2a44-46e7-a87a-ef93f4599807">WinHelp</a>
 

 

