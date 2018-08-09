---
UID: NS:winuser.tagNMHDR
title: tagNMHDR
author: windows-sdk-content
description: Contains information about a notification message.
old-location: controls\NMHDR.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\common\structures\nmhdr.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPNMHDR, NMHDR, NMHDR structure [Windows Controls], _win32_NMHDR_str, _win32_NMHDR_str_cpp, controls.NMHDR, controls._win32_NMHDR_str, richedit/NMHDR, tagNMHDR"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: NMHDR
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagNMHDR structure


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

A notification code. This member can be one of the common notification codes (see Notifications under <a href="https://msdn.microsoft.com/c8e72ae9-7c71-465d-9a6b-07e7923d4a13">General Control Reference</a>), or it can be a control-specific notification code. 

