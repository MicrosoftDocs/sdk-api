---
UID: NF:commctrl.Edit_SetExtendedStyle
title: Edit_SetExtendedStyle macro
author: windows-sdk-content
description: Sets extended styles for edit controls using the style mask. You can use this macro or send the EM_SETEXTENDEDSTYLE message explicitly.
old-location: controls\edit_setextendedstyle.htm
tech.root: controls
ms.assetid: 4ECAA174-A9C5-4A01-9341-CF6C8777E0F5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Edit_SetExtendedStyle, Edit_SetExtendedStyle macro [Windows Controls], commctrl/Edit_SetExtendedStyle, controls.edit_setextendedstyle
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
 - Commctrl.h
api_name:
 - Edit_SetExtendedStyle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Edit_SetExtendedStyle macro


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Sets extended styles for edit controls using the style mask. You can use this macro or send the <a href="https://msdn.microsoft.com/BA782136-E505-4097-8DF9-C586B1EF7FB3">EM_SETEXTENDEDSTYLE</a> message explicitly.


## -parameters




### -param hwndCtl

A handle to the edit control.


### -param dw

A <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a> value that specifies the extended edit control styles to set. 


### -param dwMask

A <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a> value that specifies which styles are to be affected. 

