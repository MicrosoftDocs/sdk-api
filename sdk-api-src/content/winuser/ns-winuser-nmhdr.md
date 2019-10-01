---
UID: NS:winuser.tagNMHDR
title: NMHDR (winuser.h)
author: windows-sdk-content
description: Contains information about a notification message.
old-location: controls\NMHDR.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\structures\nmhdr.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPNMHDR, NMHDR, NMHDR structure [Windows Controls], _win32_NMHDR_str, _win32_NMHDR_str_cpp, controls.NMHDR, controls._win32_NMHDR_str, richedit/NMHDR"
ms.topic: struct
f1_keywords: 
 - "winuser/NMHDR"
req.header: winuser.h
req.include-header: Winuser.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - richedit.h
api_name:
 - NMHDR
targetos: Windows
req.typenames: NMHDR
req.redist: 
ms.custom: 19H1
---

# NMHDR structure


## -description


Contains information about a notification message.


## -struct-fields




### -field hwndFrom

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A window handle to the control sending the message.


### -field idFrom

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT_PTR</a></b>

An identifier of the control sending the message.


### -field code

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A notification code. This member can be one of the common notification codes (see Notifications under <a href="https://docs.microsoft.com/windows/desktop/Controls/common-control-reference">General Control Reference</a>), or it can be a control-specific notification code. 

