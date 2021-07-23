---
UID: NN:shlobj_core.IActiveDesktop
title: IActiveDesktop (shlobj_core.h)
description: Allows a client program to manage the desktop items and wallpaper on a local computer.
helpviewer_keywords: ["IActiveDesktop","IActiveDesktop interface [Legacy Windows Environment Features]","IActiveDesktop interface [Legacy Windows Environment Features]","described","_win32_IActiveDesktop_Interface","lwef.iactivedesktop_interface","shell.iactivedesktop_interface","shlobj_core/IActiveDesktop"]
old-location: lwef\iactivedesktop_interface.htm
tech.root: lwef
ms.assetid: 4d572b86-36e8-417b-857c-eb477c04c691
ms.date: 12/05/2018
ms.keywords: IActiveDesktop, IActiveDesktop interface [Legacy Windows Environment Features], IActiveDesktop interface [Legacy Windows Environment Features],described, _win32_IActiveDesktop_Interface, lwef.iactivedesktop_interface, shell.iactivedesktop_interface, shlobj_core/IActiveDesktop
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IActiveDesktop
 - shlobj_core/IActiveDesktop
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
 - IActiveDesktop
---

# IActiveDesktop interface


## -description

Allows a client program to manage the desktop items and wallpaper on a local computer.

## -inheritance

The <b>IActiveDesktop</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IActiveDesktop</b> also has these types of members:

## -remarks

Your code must include Wininet.h before it includes Shlobj.h. Failure to do so will result in a compiler error.

## -see-also

<a href="/windows/desktop/lwef/active-desktop-interface">Using the Active Desktop Object</a>
