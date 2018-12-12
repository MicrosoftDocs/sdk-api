---
UID: NF:commctrl.Edit_GetFileLine
title: Edit_GetFileLine macro
author: windows-sdk-content
description: Gets the text of the specified file (or logical) line (text wrap delimiters are ignored). You can use this macro or send the EM_GETFILELINE message explicitly.
old-location: controls\edit_getfileline.htm
tech.root: controls
ms.assetid: F59ECED6-5584-43A9-A5F8-5502D66A29B6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Edit_GetFileLine, Edit_GetFileLine macro [Windows Controls], commctrl/Edit_GetFileLine, controls.edit_getfileline
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Edit_GetFileLine
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Edit_GetFileLine macro


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Gets the text of the specified file (or logical) line (text wrap delimiters are ignored). You can use this macro or send the <a href="https://msdn.microsoft.com/1BCAE1AB-F8BB-496D-9862-DA0A8A39E6F9">EM_GETFILELINE</a> message explicitly.


## -parameters




### -param hwndCtl

A handle to the edit control.


### -param lineNumber

The logical line number.


### -param textBuffer

The buffer that receives the text.


## -remarks



This macro and corresponding message do not recognize text wrapping (visible lines) and, instead, recognize file (logical) lines with an end-of-line delimiter. When text wrap is turned off, visible lines are equivalent to file lines.

The <a href="https://msdn.microsoft.com/e8e9217b-3f0c-478d-b44d-2a51868dbc5a">EM_LINEFROMCHAR</a>, <a href="https://msdn.microsoft.com/a4c65012-d47f-4d87-bc7f-2002d07f5eea">EM_LINEINDEX</a>, <a href="https://msdn.microsoft.com/cfb0632c-9ba9-4864-939a-dbbaed6c177e">EM_LINELENGTH</a>, <a href="https://msdn.microsoft.com/ff56d2c6-5013-46c6-90d8-ee2bdc9074b1">EM_GETLINE</a>, and <a href="https://msdn.microsoft.com/9fe63c10-7395-4f98-a672-14960a70d14f">EM_GETLINECOUNT</a> messages recognize visible line text wrapping and provide information for the line of text up to the wrapping line break. (Each subsequent line is delimited by the next text wrap break.)



