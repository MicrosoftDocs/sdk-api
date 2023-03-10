---
UID: NS:winuser.tagANIMATIONINFO
title: ANIMATIONINFO (winuser.h)
description: Describes the animation effects associated with user actions.
helpviewer_keywords: ["*LPANIMATIONINFO","ANIMATIONINFO","ANIMATIONINFO structure [Windows and Messages]","LPANIMATIONINFO","LPANIMATIONINFO structure pointer [Windows and Messages]","_win32_animationinfo_str","animationinfo_str_cpp","base.animationinfo_str","tagANIMATIONINFO","winmsg.animationinfo_str","winui.animationinfo_str","winuser/ANIMATIONINFO","winuser/LPANIMATIONINFO"]
old-location: winmsg\animationinfo_str.htm
tech.root: winmsg
ms.assetid: 37f2e434-d98a-42f5-b9a8-90f93768faae
ms.date: 12/05/2018
ms.keywords: '*LPANIMATIONINFO, ANIMATIONINFO, ANIMATIONINFO structure [Windows and Messages], LPANIMATIONINFO, LPANIMATIONINFO structure pointer [Windows and Messages], _win32_animationinfo_str, animationinfo_str_cpp, base.animationinfo_str, tagANIMATIONINFO, winmsg.animationinfo_str, winui.animationinfo_str, winuser/ANIMATIONINFO, winuser/LPANIMATIONINFO'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ANIMATIONINFO, *LPANIMATIONINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagANIMATIONINFO
 - winuser/tagANIMATIONINFO
 - LPANIMATIONINFO
 - winuser/LPANIMATIONINFO
 - ANIMATIONINFO
 - winuser/ANIMATIONINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - ANIMATIONINFO
---

# ANIMATIONINFO structure


## -description

Describes the animation effects associated with user actions. This structure is used with the 
<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a> function when the SPI_GETANIMATION or SPI_SETANIMATION action value is specified.

## -struct-fields

### -field cbSize

The size of the structure, in bytes. The caller must set this to <code>sizeof(ANIMATIONINFO)</code>.

### -field iMinAnimate

If this member is nonzero, minimize and restore animation is enabled; otherwise it is disabled.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>