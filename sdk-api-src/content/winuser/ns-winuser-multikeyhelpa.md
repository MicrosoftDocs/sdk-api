---
UID: NS:winuser.tagMULTIKEYHELPA
title: MULTIKEYHELPA (winuser.h)
description: Specifies a keyword to search for and the keyword table to be searched by Windows Help.
helpviewer_keywords: ["*LPMULTIKEYHELPA","*PMULTIKEYHELPA","MULTIKEYHELP","MULTIKEYHELP structure [Windows Shell]","MULTIKEYHELPA","_win32_MULTIKEYHELP_str","shell.MULTIKEYHELP_str","tagMULTIKEYHELPA","tagMULTIKEYHELPW","winuser/MULTIKEYHELP"]
old-location: shell\MULTIKEYHELP_str.htm
tech.root: shell
ms.assetid: 5fe0cd44-196c-4d9a-b9f8-2a97a92f2545
ms.date: 12/05/2018
ms.keywords: '*LPMULTIKEYHELPA, *PMULTIKEYHELPA, MULTIKEYHELP, MULTIKEYHELP structure [Windows Shell], MULTIKEYHELPA, _win32_MULTIKEYHELP_str, shell.MULTIKEYHELP_str, tagMULTIKEYHELPA, tagMULTIKEYHELPW, winuser/MULTIKEYHELP'
f1_keywords:
- winuser/MULTIKEYHELP
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Winuser.h
api_name:
- MULTIKEYHELP
targetos: Windows
req.typenames: MULTIKEYHELPA, *PMULTIKEYHELPA, *LPMULTIKEYHELPA
req.redist: 
ms.custom: 19H1
---

# MULTIKEYHELPA structure


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




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-winhelpa">WinHelp</a>
 

 

