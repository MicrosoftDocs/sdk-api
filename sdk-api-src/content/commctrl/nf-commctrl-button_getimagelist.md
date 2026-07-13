---
UID: NF:commctrl.Button_GetImageList
title: Button_GetImageList macro (commctrl.h)
description: Gets the BUTTON_IMAGELIST structure that describes the image list that is set for a button control. You can use this macro or send the BCM_GETIMAGELIST message explicitly.
helpviewer_keywords: ["Button_GetImageList","Button_GetImageList macro [Windows Controls]","_win32_Button_GetImageList","_win32_Button_GetImageList_cpp","commctrl/Button_GetImageList","controls.Button_GetImageList","controls._win32_Button_GetImageList"]
old-location: controls\Button_GetImageList.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_getimagelist.htm
ms.date: 10/21/2024
ms.keywords: Button_GetImageList, Button_GetImageList macro [Windows Controls], _win32_Button_GetImageList, _win32_Button_GetImageList_cpp, commctrl/Button_GetImageList, controls.Button_GetImageList, controls._win32_Button_GetImageList
req.header: commctrl.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Button_GetImageList
 - commctrl/Button_GetImageList
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
 - Button_GetImageList
---

# Button_GetImageList macro

## -syntax

```cpp
BOOL Button_GetImageList(
   HWND              hwnd,
   PBUTTON_IMAGELIST pbuttonImagelist
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

If the macro succeeds, it returns <b>TRUE</b>. Otherwise it returns <b>FALSE</b>.


## -description

Gets the <a href="/windows/desktop/api/commctrl/ns-commctrl-button_imagelist">BUTTON_IMAGELIST</a> structure that describes the image list that is set for a button control. You can use this macro or send the <a href="/windows/desktop/Controls/bcm-getimagelist">BCM_GETIMAGELIST</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the button control.

### -param pbuttonImagelist

Type: <b>PBUTTON_IMAGELIST</b>

A pointer to a <a href="/windows/desktop/api/commctrl/ns-commctrl-button_imagelist">BUTTON_IMAGELIST</a> structure that contains image list information.

## -remarks

<div class="alert"><b>Note</b>  To use this macro, you must provide a manifest specifying Comctl32.dll version 6.0. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Controls/bcm-getimagelist">BCM_GETIMAGELIST</a>



<a href="/windows/desktop/api/commctrl/ns-commctrl-button_imagelist">BUTTON_IMAGELIST</a>



<b>Reference</b>
