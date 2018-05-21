---
UID: NF:shdeprecated.ITrackShellMenu.SetObscured
title: ITrackShellMenu::SetObscured
author: windows-driver-content
description: Coordinates obscured items on a toolbar with items in a menu.
old-location: shell\ITrackShellMenu_SetObscured.htm
old-project: shell
ms.assetid: a8b73bdb-95dd-4ca7-8dc9-3318faf37338
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: ITrackShellMenu interface [Windows Shell],SetObscured method, ITrackShellMenu.SetObscured, ITrackShellMenu::SetObscured, SMSET_BOTTOM, SMSET_DONTOWN, SMSET_TOP, SetObscured, SetObscured method [Windows Shell], SetObscured method [Windows Shell],ITrackShellMenu interface, _shell_ITrackShellMenu_SetObscured, shdeprecated/ITrackShellMenu::SetObscured, shell.ITrackShellMenu_SetObscured
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: BNSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	ITrackShellMenu.SetObscured
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 4.0
---

# ITrackShellMenu::SetObscured


## -description


Coordinates obscured items on a toolbar with items in a menu.


## -parameters




### -param hwndTB [in]

Type: <b>HWND</b>

A handle to a toolbar control whose buttons have command IDs that correspond to menu IDs in the tracked menu.


### -param punkBand [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

If this parameter points to a COM object that supports the <a href="https://msdn.microsoft.com/46793ae9-936e-4a58-bc34-84396151b4a3">IShellMenu</a> interface, menu items that correspond to visible toolbar buttons are filtered out of the menu so that they do not appear in both places. 
                
                    

If this parameter is <b>NULL</b> or points to a COM object that does not support the <a href="https://msdn.microsoft.com/46793ae9-936e-4a58-bc34-84396151b4a3">IShellMenu</a> interface, then the obscured buttons in the toolbar are added to the shell menu in the position specified in <i>dwSMSetFlags</i>.


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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Obscured buttons are those buttons that cannot be displayed due to toolbar size limitations. Commonly, to see them you must press the chevron at the end of the toolbar.



