---
UID: NF:winuser.MAKEINTRESOURCEA
title: MAKEINTRESOURCEA macro (winuser.h)
description: Converts an integer value to a resource type compatible with the resource-management functions. This macro is used in place of a string containing the name of the resource.
helpviewer_keywords: ["MAKEINTRESOURCE","MAKEINTRESOURCE macro [Menus and Other Resources]","MAKEINTRESOURCEA","MAKEINTRESOURCEW","_win32_MAKEINTRESOURCE","_win32_makeintresource_cpp","menurc.makeintresource","winui._win32_makeintresource","winuser/MAKEINTRESOURCE"]
old-location: menurc\makeintresource.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcemacros\makeintresource.htm
ms.date: 12/05/2018
ms.keywords: MAKEINTRESOURCE, MAKEINTRESOURCE macro [Menus and Other Resources], MAKEINTRESOURCEA, MAKEINTRESOURCEW, _win32_MAKEINTRESOURCE, _win32_makeintresource_cpp, menurc.makeintresource, winui._win32_makeintresource, winuser/MAKEINTRESOURCE
f1_keywords:
- winuser/MAKEINTRESOURCE
dev_langs:
- c++
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
- MAKEINTRESOURCE
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MAKEINTRESOURCEA macro


## -description


Converts an integer value to a resource type compatible with the resource-management functions. This macro is used in place of a string containing the name of the resource. 


## -parameters




### -param i

The integer value to be converted. 


## -remarks



The return value should be passed only to functions which explicitly indicate that they accept <b>MAKEINTRESOURCE</b> as a parameter. For example, the resource management functions allow the return value of <b>MAKEINTRESOURCE</b> to be passed as the <i>lpType</i> or <i>lpName</i> parameters. 





> [!NOTE]
> The winuser.h header defines MAKEINTRESOURCE as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also




<a href="https://docs.microsoft.com/windows/desktop/menurc/resources">Resources Overview</a>
 

 

