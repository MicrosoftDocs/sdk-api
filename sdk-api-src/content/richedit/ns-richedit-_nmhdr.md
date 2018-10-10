---
UID: NS:richedit._nmhdr
title: "_nmhdr"
author: windows-sdk-content
description: Contains information about a notification message.
old-location: controls\NMHDR.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\structures\nmhdr.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: NMHDR, NMHDR structure [Windows Controls], _nmhdr, _win32_NMHDR_str, _win32_NMHDR_str_cpp, controls.NMHDR, controls._win32_NMHDR_str, richedit/NMHDR
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: richedit.h
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
product: Windows
targetos: Windows
req.typenames: NMHDR
req.redist: 
---

# _nmhdr structure


## -description


Contains information about a notification message.


## -struct-fields




### -field hwndFrom

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A window handle to the control sending the message.


### -field idFrom

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT_PTR</a></b>

An identifier of the control sending the message.


### -field code

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A notification code. This member can be one of the common notification codes (see Notifications under <a href="https://msdn.microsoft.com/en-us/library/Bb775497(v=VS.85).aspx">General Control Reference</a>), or it can be a control-specific notification code. 

