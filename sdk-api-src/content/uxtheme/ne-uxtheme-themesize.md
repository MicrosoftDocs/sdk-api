---
UID: NE:uxtheme.THEMESIZE
title: THEMESIZE
author: windows-sdk-content
description: Identifies the type of size value to retrieve for a visual style part.
old-location: controls\THEME_SIZE.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\userex\enums\themesize.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: THEMESIZE, THEMESIZE enumeration [Windows Controls], THEME_SIZE, THEME_SIZE enumeration [Windows Controls], TS_DRAW, TS_MIN, TS_TRUE, controls.THEME_SIZE, controls.inet_THEME_SIZE, inet_THEME_SIZE, inet_THEME_SIZE_cpp, uxtheme/THEMESIZE, uxtheme/TS_DRAW, uxtheme/TS_MIN, uxtheme/TS_TRUE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - THEME_SIZE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# THEMESIZE enumeration


## -description


Identifies the type of size value to retrieve for a visual style part.


## -enum-fields




### -field TS_MIN

Receives the minimum size of a visual style part.


### -field TS_TRUE

Receives the size of the visual style part that will best fit the available space.


### -field TS_DRAW

Receives the size that the theme manager uses to draw a part.


## -remarks



A value from the <b>THEMESIZE</b> enumeration is used with the <a href="https://msdn.microsoft.com/en-us/library/Bb759759(v=VS.85).aspx">GetThemePartSize</a> function to specify the type of size value to retrieve for a particular visual style part. 



