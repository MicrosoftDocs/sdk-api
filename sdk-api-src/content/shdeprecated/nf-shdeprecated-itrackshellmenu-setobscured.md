---
UID: NF:shdeprecated.ITrackShellMenu.SetObscured
title: ITrackShellMenu::SetObscured (shdeprecated.h)
description: Coordinates obscured items on a toolbar with items in a menu.
helpviewer_keywords: ["ITrackShellMenu interface [Windows Shell]","SetObscured method","ITrackShellMenu.SetObscured","ITrackShellMenu::SetObscured","SMSET_BOTTOM","SMSET_DONTOWN","SMSET_TOP","SetObscured","SetObscured method [Windows Shell]","SetObscured method [Windows Shell]","ITrackShellMenu interface","_shell_ITrackShellMenu_SetObscured","shdeprecated/ITrackShellMenu::SetObscured","shell.ITrackShellMenu_SetObscured"]
old-location: shell\ITrackShellMenu_SetObscured.htm
tech.root: shell
ms.assetid: a8b73bdb-95dd-4ca7-8dc9-3318faf37338
ms.date: 12/05/2018
ms.keywords: ITrackShellMenu interface [Windows Shell],SetObscured method, ITrackShellMenu.SetObscured, ITrackShellMenu::SetObscured, SMSET_BOTTOM, SMSET_DONTOWN, SMSET_TOP, SetObscured, SetObscured method [Windows Shell], SetObscured method [Windows Shell],ITrackShellMenu interface, _shell_ITrackShellMenu_SetObscured, shdeprecated/ITrackShellMenu::SetObscured, shell.ITrackShellMenu_SetObscured
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
 - ITrackShellMenu::SetObscured
 - shdeprecated/ITrackShellMenu::SetObscured
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
 - ITrackShellMenu.SetObscured
---

# ITrackShellMenu::SetObscured


## -description

Coordinates obscured items on a toolbar with items in a menu.

## -parameters

### -param hwndTB [in]

Type: <b>HWND</b>

A handle to a toolbar control whose buttons have command IDs that correspond to menu IDs in the tracked menu.

### -param punkBand [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

If this parameter points to a COM object that supports the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu">IShellMenu</a> interface, menu items that correspond to visible toolbar buttons are filtered out of the menu so that they do not appear in both places. 
                
                    

If this parameter is <b>NULL</b> or points to a COM object that does not support the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu">IShellMenu</a> interface, then the obscured buttons in the toolbar are added to the shell menu in the position specified in <i>dwSMSetFlags</i>.

### -param dwSMSetFlags [in]

Type: <b>DWORD</b>

One of the following values.



#### SMSET_TOP (0x10000000)

New menu items are added at the top of the menu.



#### SMSET_BOTTOM (0x20000000)

New menu items are added at the bottom of the menu.



#### SMSET_DONTOWN

Reserved; do not use.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Obscured buttons are those buttons that cannot be displayed due to toolbar size limitations. Commonly, to see them you must press the chevron at the end of the toolbar.