---
UID: NF:shdeprecated.ITrackShellMenu.Popup
title: ITrackShellMenu::Popup (shdeprecated.h)
description: Displays a modal pop-up menu at a specific location.
helpviewer_keywords: ["ITrackShellMenu interface [Windows Shell]","Popup method","ITrackShellMenu.Popup","ITrackShellMenu::Popup","Popup","Popup method [Windows Shell]","Popup method [Windows Shell]","ITrackShellMenu interface","_shell_ITrackShellMenu_Popup","shdeprecated/ITrackShellMenu::Popup","shell.ITrackShellMenu_Popup"]
old-location: shell\ITrackShellMenu_Popup.htm
tech.root: shell
ms.assetid: a8098143-6f36-496c-81af-f06fb83c9920
ms.date: 12/05/2018
ms.keywords: ITrackShellMenu interface [Windows Shell],Popup method, ITrackShellMenu.Popup, ITrackShellMenu::Popup, Popup, Popup method [Windows Shell], Popup method [Windows Shell],ITrackShellMenu interface, _shell_ITrackShellMenu_Popup, shdeprecated/ITrackShellMenu::Popup, shell.ITrackShellMenu_Popup
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITrackShellMenu::Popup
 - shdeprecated/ITrackShellMenu::Popup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ITrackShellMenu.Popup
---

# ITrackShellMenu::Popup


## -description

Displays a modal pop-up menu at a specific location.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

The handle of the parent window of the pop-up menu.

### -param ppt [in]

Type: <b><a href="/windows/win32/api/windef/ns-windef-pointl">POINTL</a>*</b>

A pointer to a <a href="/windows/win32/api/windef/ns-windef-pointl">POINTL</a> structure that specifies an initial point in screen coordinates. The pop-up menu is displayed in relation to this point as determined by the position flags set in <i>dwFlags</i>.

### -param prcExclude [in]

Type: <b><a href="/windows/win32/api/windef/ns-windef-rectl">RECTL</a>*</b>

A pointer to a <a href="/windows/win32/api/windef/ns-windef-rectl">RECTL</a> structure that specifies the rectangle to exclude when positioning the menu. The alignment of the menu in relation to this area is determined by the alignment flags set in <i>dwFlags</i>. This parameter can be set to <b>NULL</b>.

### -param dwFlags [in]

Type: <b>MP_POPUPFLAGS</b>

One or more of the <a href="/windows/desktop/shell/mp-popupflags">MP_POPUPFLAGS</a> constants that specify options involved in the display of the pop-up menu.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.