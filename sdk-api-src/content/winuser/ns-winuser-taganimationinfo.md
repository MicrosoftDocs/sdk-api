---
UID: NS:winuser.tagANIMATIONINFO
title: tagANIMATIONINFO
author: windows-sdk-content
description: Describes the animation effects associated with user actions.
old-location: winmsg\animationinfo_str.htm
tech.root: winmsg
ms.assetid: 37f2e434-d98a-42f5-b9a8-90f93768faae
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPANIMATIONINFO, ANIMATIONINFO, ANIMATIONINFO structure [Windows and Messages], LPANIMATIONINFO, LPANIMATIONINFO structure pointer [Windows and Messages], _win32_animationinfo_str, animationinfo_str_cpp, base.animationinfo_str, tagANIMATIONINFO, winmsg.animationinfo_str, winui.animationinfo_str, winuser/ANIMATIONINFO, winuser/LPANIMATIONINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - ANIMATIONINFO
product: Windows
targetos: Windows
req.typenames: ANIMATIONINFO, *LPANIMATIONINFO
req.redist: 
---

# tagANIMATIONINFO structure


## -description


Describes the animation effects associated with user actions. This structure is used with the 
<a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a> function when the SPI_GETANIMATION or SPI_SETANIMATION action value is specified.


## -struct-fields




### -field cbSize

The size of the structure, in bytes. The caller must set this to <code>sizeof(ANIMATIONINFO)</code>.


### -field iMinAnimate

If this member is nonzero, minimize and restore animation is enabled; otherwise it is disabled.


## -see-also




<a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>
 

 

