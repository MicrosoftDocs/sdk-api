---
UID: NF:shdeprecated.ITrackShellMenu.Popup
title: ITrackShellMenu::Popup
author: windows-sdk-content
description: Displays a modal pop-up menu at a specific location.
old-location: shell\ITrackShellMenu_Popup.htm
old-project: shell
ms.assetid: a8098143-6f36-496c-81af-f06fb83c9920
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ITrackShellMenu interface [Windows Shell],Popup method, ITrackShellMenu.Popup, ITrackShellMenu::Popup, Popup, Popup method [Windows Shell], Popup method [Windows Shell],ITrackShellMenu interface, _shell_ITrackShellMenu_Popup, shdeprecated/ITrackShellMenu::Popup, shell.ITrackShellMenu_Popup
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BNSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	ITrackShellMenu.Popup
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 4.0
---

# ITrackShellMenu::Popup


## -description


Displays a modal pop-up menu at a specific location.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

The handle of the parent window of the pop-up menu.


### -param ppt [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structure that specifies an initial point in screen coordinates. The pop-up menu is displayed in relation to this point as determined by the position flags set in <i>dwFlags</i>.


### -param prcExclude [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a> structure that specifies the rectangle to exclude when positioning the menu. The alignment of the menu in relation to this area is determined by the alignment flags set in <i>dwFlags</i>. This parameter can be set to <b>NULL</b>.


### -param dwFlags [in]

Type: <b>MP_POPUPFLAGS</b>

One or more of the <a href="https://msdn.microsoft.com/cc1d9ff0-a03b-4bd3-b481-9b78d20eb771">MP_POPUPFLAGS</a> constants that specify options involved in the display of the pop-up menu.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



