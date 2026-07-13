---
UID: NN:shdeprecated.ITrackShellMenu
title: ITrackShellMenu (shdeprecated.h)
description: Exposes methods that extend the IShellMenu interface by providing the ability to coordinate toolbar buttons with a menu as well as display a pop-up menu.
helpviewer_keywords: ["ITrackShellMenu","ITrackShellMenu interface [Windows Shell]","ITrackShellMenu interface [Windows Shell]","described","_shell_ITrackShellMenu","shdeprecated/ITrackShellMenu","shell.ITrackShellMenu"]
old-location: shell\ITrackShellMenu.htm
tech.root: shell
ms.assetid: 187796db-2932-482e-833a-b4674f009b71
ms.date: 12/05/2018
ms.keywords: ITrackShellMenu, ITrackShellMenu interface [Windows Shell], ITrackShellMenu interface [Windows Shell],described, _shell_ITrackShellMenu, shdeprecated/ITrackShellMenu, shell.ITrackShellMenu
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITrackShellMenu
 - shdeprecated/ITrackShellMenu
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - ITrackShellMenu
---

# ITrackShellMenu interface


## -description

Exposes methods that extend the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu">IShellMenu</a> interface by providing the ability to coordinate toolbar buttons with a menu as well as display a pop-up menu.

## -inheritance

The <b>ITrackShellMenu</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu">IShellMenu</a>. <b>ITrackShellMenu</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu">IShellMenu</a> interface, from which it inherits.

This interface is implemented by the track Shell menu object. You can obtain that object by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with a class identifier (CLSID) of <code>CLSID_TrackShellMenu</code>. You can obtain interface pointers using standard Component Object Model (COM) procedures. The value of CLSID_TrackShellMenu is {8278F931-2A3E-11d2-838F-00C04FD918D0}.
