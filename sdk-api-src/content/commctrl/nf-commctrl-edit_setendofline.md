---
UID: NF:commctrl.Edit_SetEndOfLine
title: Edit_SetEndOfLine macro (commctrl.h)
description: Sets the end of line character used for the content of the edit control. You can use this macro or send the EM_SETENDOFLINE message explicitly.
old-location: controls\edit_setendofline.htm
tech.root: Controls
ms.assetid: D143B914-5F68-4957-9D1F-C55977E27C8B
ms.date: 12/05/2018
ms.keywords: Edit_SetEndOfLine, Edit_SetEndOfLine macro [Windows Controls], commctrl/Edit_SetEndOfLine, controls.edit_setendofline
f1_keywords:
- commctrl/Edit_SetEndOfLine
dev_langs:
- c++
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
- Edit_SetEndOfLine
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Edit_SetEndOfLine macro


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Sets the end of line character used for the content of the edit control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/controls/em-setendofline">EM_SETENDOFLINE</a> message explicitly. 


## -parameters




### -param hwndCtl

A handle to the edit control.


### -param eolType

The end of line character to use.

