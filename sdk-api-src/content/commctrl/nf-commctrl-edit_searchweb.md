---
UID: NF:commctrl.Edit_SearchWeb
title: Edit_SearchWeb macro (commctrl.h)
description: Invokes the &quot;Search with Bing…&quot; context menu item in edit controls. You can use this macro or send the EM_SEARCHWEB message explicitly.
helpviewer_keywords: ["Edit_SearchWeb","Edit_SearchWeb macro [Windows Controls]","commctrl/Edit_SearchWeb","controls.edit_searchweb"]
old-location: controls\edit_searchweb.htm
tech.root: Controls
ms.assetid: 33F79879-EC55-438F-AC55-14BC119A4EFC
ms.date: 07/01/2025
ms.keywords: Edit_SearchWeb, Edit_SearchWeb macro [Windows Controls], commctrl/Edit_SearchWeb, controls.edit_searchweb
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Edit_SearchWeb
 - commctrl/Edit_SearchWeb
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - Edit_SearchWeb
---

# Edit_SearchWeb macro

## -syntax

```cpp
void Edit_SearchWeb(
    HWND hwndCtl
);
```


## -description



Invokes the "Search with Bing…" context menu item in edit controls. You can use this macro or send the <a href="/windows/desktop/controls/em-searchweb">EM_SEARCHWEB</a> message explicitly.

## -parameters

### -param hwndCtl

A handle to the edit control.
