---
UID: NS:uxtheme._WTA_OPTIONS
title: WTA_OPTIONS (uxtheme.h)
description: Defines options that are used to set window visual style attributes.
old-location: controls\WTA_OPTIONS.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\structures\wta_options.htm
ms.date: 12/05/2018
ms.keywords: '*PWTA_OPTIONS, PWTA_OPTIONS, PWTA_OPTIONS structure pointer [Windows Controls], WTA_OPTIONS, WTA_OPTIONS structure [Windows Controls], controls.WTA_OPTIONS, controls.inet_WTA_OPTIONS, inet_WTA_OPTIONS, inet_WTA_OPTIONS_cpp, uxtheme/PWTA_OPTIONS, uxtheme/WTA_OPTIONS'
f1_keywords:
- uxtheme/WTA_OPTIONS
dev_langs:
- c++
req.header: uxtheme.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Uxtheme.h
api_name:
- WTA_OPTIONS
targetos: Windows
req.typenames: WTA_OPTIONS, *PWTA_OPTIONS
req.redist: 
ms.custom: 19H1
---

# WTA_OPTIONS structure


## -description


Defines options that are used to set window visual style attributes.


## -struct-fields




### -field dwFlags

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A combination of flags that modify window visual style attributes. Can be a combination of the <a href="https://docs.microsoft.com/windows/desktop/Controls/wtnca">WTNCA</a> constants.


### -field dwMask

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A bitmask that describes how the values specified in <b>dwFlags</b> should be applied. If the bit corresponding to a value in <b>dwFlags</b> is 0, that flag will be removed. If the bit is 1, the flag will be added.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uxtheme/nf-uxtheme-setwindowthemeattribute">SetWindowThemeAttribute</a>
 

 

