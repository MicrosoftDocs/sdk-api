---
UID: NF:commctrl.Edit_GetFileLineCount
title: Edit_GetFileLineCount macro (commctrl.h)
description: Gets the number of file (or logical) lines (text wrap delimiters are ignored). You can use this macro or send the EM_GETFILELINECOUNT message explicitly.helpviewer_keywords: ["Edit_GetFileLineCount","Edit_GetFileLineCount macro [Windows Controls]","commctrl/Edit_GetFileLineCount","controls.edit_getfilelinecount"]
old-location: controls\edit_getfilelinecount.htm
tech.root: Controls
ms.assetid: FEE1018B-AE00-4934-9C64-AB7A679E6A8C
ms.date: 12/05/2018
ms.keywords: Edit_GetFileLineCount, Edit_GetFileLineCount macro [Windows Controls], commctrl/Edit_GetFileLineCount, controls.edit_getfilelinecount
f1_keywords:
- commctrl/Edit_GetFileLineCount
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
- Edit_GetFileLineCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Edit_GetFileLineCount macro


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Gets the number of file (or logical) lines (text wrap delimiters are ignored). You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/controls/em-getfilelinecount">EM_GETFILELINECOUNT</a> message explicitly.


## -parameters




### -param hwndCtl

A handle to the edit control.


## -remarks



This macro and corresponding message do not recognize text wrapping (visible lines) and, instead, recognize file (logical) lines with an end-of-line delimiter. When text wrap is turned off, visible lines are equivalent to file lines.

The <a href="https://docs.microsoft.com/windows/desktop/Controls/em-linefromchar">EM_LINEFROMCHAR</a>, <a href="https://docs.microsoft.com/windows/desktop/controls/em-lineindex">EM_LINEINDEX</a>, <a href="https://docs.microsoft.com/windows/desktop/Controls/em-linelength">EM_LINELENGTH</a>, <a href="https://docs.microsoft.com/windows/desktop/Controls/em-getline">EM_GETLINE</a>, and <a href="https://docs.microsoft.com/windows/desktop/Controls/em-getlinecount">EM_GETLINECOUNT</a> messages recognize visible line text wrapping and provide information for the line of text up to the wrapping line break. (Each subsequent line is delimited by the next text wrap break.)



