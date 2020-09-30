---
UID: NF:commctrl.Button_SetImageList
title: Button_SetImageList macro (commctrl.h)
description: Assigns an image list to a button control. You can use this macro or send the BCM_SETIMAGELIST message explicitly.
helpviewer_keywords: ["Button_SetImageList","Button_SetImageList macro [Windows Controls]","_win32_Button_SetImageList","_win32_Button_SetImageList_cpp","commctrl/Button_SetImageList","controls.Button_SetImageList","controls._win32_Button_SetImageList"]
old-location: controls\Button_SetImageList.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_setimagelist.htm
ms.date: 12/05/2018
ms.keywords: Button_SetImageList, Button_SetImageList macro [Windows Controls], _win32_Button_SetImageList, _win32_Button_SetImageList_cpp, commctrl/Button_SetImageList, controls.Button_SetImageList, controls._win32_Button_SetImageList
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
 - Button_SetImageList
 - commctrl/Button_SetImageList
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
 - Button_SetImageList
---

# Button_SetImageList macro


## -description

Assigns an image list to a button control. You can use this macro or send the <a href="/windows/desktop/Controls/bcm-setimagelist">BCM_SETIMAGELIST</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the button control.

### -param pbuttonImagelist

Type: <b>PBUTTON_IMAGELIST</b>

A pointer to a <a href="/windows/desktop/api/commctrl/ns-commctrl-button_imagelist">BUTTON_IMAGELIST</a> structure that contains the image list information to set.

## -remarks

<div class="alert"><b>Note</b>  To use this macro, you must provide a manifest specifying Comclt32.dll version 6.0. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.</div>
<div> </div>