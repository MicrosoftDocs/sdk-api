---
UID: NN:shlobj.INewShortcutHookA
title: INewShortcutHookA (shlobj.h)
description: Exposes methods to create a new Internet shortcut. (ANSI)
helpviewer_keywords: ["INewShortcutHook","INewShortcutHook interface [Windows Shell]","INewShortcutHook interface [Windows Shell]","described","INewShortcutHookA","INewShortcutHookW","_win32_INewShortcutHook","shell.INewShortcutHook","shlobj/INewShortcutHook"]
old-location: shell\INewShortcutHook.htm
tech.root: shell
ms.assetid: 5a097e96-178a-44bd-9d3d-ed53338b97d5
ms.date: 12/05/2018
ms.keywords: INewShortcutHook, INewShortcutHook interface [Windows Shell], INewShortcutHook interface [Windows Shell],described, INewShortcutHookA, INewShortcutHookW, _win32_INewShortcutHook, shell.INewShortcutHook, shlobj/INewShortcutHook
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INewShortcutHookA
 - shlobj/INewShortcutHookA
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
 - INewShortcutHook
---

# INewShortcutHookA interface


## -description

Exposes methods to create a new Internet shortcut.

## -inheritance

The <b>INewShortcutHook</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INewShortcutHook</b> also has these types of members:

## -remarks

You do not typically implement <b>INewShortcutHook</b>. It is implemented by the Shell for Internet shortcuts.

You use <b>INewShortcutHook</b> when creating a new Internet shortcut. The methods provided by this interface are supplied as a convenience.

<b>INewShortcutHook</b> is derived from <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>. The listed methods are specific to <b>INewShortcutHook</b>.




> [!NOTE]
> The shlobj.h header defines INewShortcutHook as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
