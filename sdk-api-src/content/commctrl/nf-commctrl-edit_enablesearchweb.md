---
UID: NF:commctrl.Edit_EnableSearchWeb
title: Edit_EnableSearchWeb macro (commctrl.h)
author: windows-sdk-content
description: Enables or disables the &#0034;Search with Bing…&#0034; context menu item in edit controls. You can use this macro or send the EM_ENABLESEARCHWEB message explicitly.
old-location: controls\edit_enablesearchweb.htm
tech.root: Controls
ms.assetid: BB56F4F6-0D13-41B4-B8C1-FF724FCC4D0B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Edit_EnableSearchWeb, Edit_EnableSearchWeb macro [Windows Controls], commctrl/Edit_EnableSearchWeb, controls.edit_enablesearchweb
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
 - Edit_EnableSearchWeb
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Edit_EnableSearchWeb macro


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Enables or disables the "Search with Bing…" context menu item in edit controls. You can use this macro or send the <a href="https://msdn.microsoft.com/1E761CB2-80CC-4DC7-8E54-54A2BD8572FB">EM_ENABLESEARCHWEB</a> message explicitly. 


## -parameters




### -param hwndCtl

A handle to the edit control.


### -param enable

<b>TRUE</b> to enable web search, or <b>FALSE</b> to disable it.

