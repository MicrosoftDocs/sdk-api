---
UID: NF:commctrl.Edit_GetZoom
title: Edit_GetZoom macro
author: windows-sdk-content
description: Gets the current zoom ratio of an edit control (the zoom ratio is always between 1/64 and 64). You can use this macro or send the EM_GETZOOM message explicitly.
old-location: controls\edit_getzoom.htm
tech.root: Controls
ms.assetid: 74125732-4797-4DA0-A465-650B286A724C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Edit_GetZoom, Edit_GetZoom macro [Windows Controls], commctrl/Edit_GetZoom, controls.edit_getzoom
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
 - Edit_GetZoom
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Edit_GetZoom macro


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Gets the current zoom ratio of an edit control (the zoom ratio is always between 1/64 and 64). You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774208(v=VS.85).aspx">EM_GETZOOM</a> message explicitly.


## -parameters




### -param hwndCtl

A handle to the edit control.


### -param numerator [out]

The numerator of the ratio as a fraction.


### -param denominator [out]

The denominator of the ratio as a fraction.

