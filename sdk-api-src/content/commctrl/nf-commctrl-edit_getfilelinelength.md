---
UID: NF:commctrl.Edit_GetFileLineLength
title: Edit_GetFileLineLength macro
author: windows-sdk-content
description: Gets the length of the file (or logical) line of text from the specified character index (text wrap delimiters are ignored). You can use this macro or send the EM_FILELINELENGTH message explicitly.
old-location: controls\edit_getfilelinelength.htm
tech.root: Controls
ms.assetid: 04315431-FC5C-41FB-9806-7904F71C19FD
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Edit_GetFileLineLength, Edit_GetFileLineLength macro [Windows Controls], commctrl/Edit_GetFileLineLength, controls.edit_getfilelinelength
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
 - Edit_GetFileLineLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Edit_GetFileLineLength macro


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Gets the length of the file (or logical) line of text from the specified character index  (text wrap delimiters are ignored). You can use this macro or send the <a href="https://msdn.microsoft.com/B8F4039B-5969-4384-ABFF-D06FB451A278">EM_FILELINELENGTH</a> message explicitly.


## -parameters




### -param hwndCtl

A handle to the edit control.


### -param characterIndex

The character index. If characterIndex = -1, the caret location index is used, not including the
        length of any selected text.


## -remarks



The character index is the zero-based index of the character from the beginning of the edit control. 

This macro and corresponding message do not recognize text wrapping (visible lines) and, instead, recognize file (logical) lines with an end-of-line delimiter. When text wrap is turned off, visible lines are equivalent to file lines.

The <a href="https://msdn.microsoft.com/en-us/library/Bb761609(v=VS.85).aspx">EM_LINEFROMCHAR</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb761611(v=VS.85).aspx">EM_LINEINDEX</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb761613(v=VS.85).aspx">EM_LINELENGTH</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb761584(v=VS.85).aspx">EM_GETLINE</a>, and <a href="https://msdn.microsoft.com/en-us/library/Bb761586(v=VS.85).aspx">EM_GETLINECOUNT</a> messages recognize visible line text wrapping and provide information for the line of text up to the wrapping line break. (Each subsequent line is delimited by the next text wrap break.)



