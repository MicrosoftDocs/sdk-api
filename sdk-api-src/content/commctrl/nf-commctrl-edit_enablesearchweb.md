---
UID: NF:commctrl.Edit_EnableSearchWeb
title: Edit_EnableSearchWeb macro (commctrl.h)
description: Enables or disables the &quot;Search with Bing…&quot; context menu item in edit controls. You can use this macro or send the EM_ENABLESEARCHWEB message explicitly.
helpviewer_keywords: ["Edit_EnableSearchWeb","Edit_EnableSearchWeb macro [Windows Controls]","commctrl/Edit_EnableSearchWeb","controls.edit_enablesearchweb"]
old-location: controls\edit_enablesearchweb.htm
tech.root: Controls
ms.assetid: BB56F4F6-0D13-41B4-B8C1-FF724FCC4D0B
ms.date: 12/05/2018
ms.keywords: Edit_EnableSearchWeb, Edit_EnableSearchWeb macro [Windows Controls], commctrl/Edit_EnableSearchWeb, controls.edit_enablesearchweb
f1_keywords:
- commctrl/Edit_EnableSearchWeb
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
- Edit_EnableSearchWeb
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Edit_EnableSearchWeb macro


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Enables or disables the "Search with Bing…" context menu item in edit controls. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/controls/em-enablesearchweb">EM_ENABLESEARCHWEB</a> message explicitly. 


## -parameters




### -param hwndCtl

A handle to the edit control.


### -param enable

<b>TRUE</b> to enable web search, or <b>FALSE</b> to disable it.

