---
UID: NF:winuser.IS_INTRESOURCE
title: IS_INTRESOURCE macro (winuser.h)
description: Determines whether a value is an integer identifier for a resource.
helpviewer_keywords: ["IS_INTRESOURCE","IS_INTRESOURCE macro [Menus and Other Resources]","_win32_IS_INTRESOURCE","_win32_is_intresource_cpp","menurc.is_intresource","winui._win32_is_intresource","winuser/IS_INTRESOURCE"]
old-location: menurc\is_intresource.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcemacros\is_intresource.htm
ms.date: 12/05/2018
ms.keywords: IS_INTRESOURCE, IS_INTRESOURCE macro [Menus and Other Resources], _win32_IS_INTRESOURCE, _win32_is_intresource_cpp, menurc.is_intresource, winui._win32_is_intresource, winuser/IS_INTRESOURCE
f1_keywords:
- winuser/IS_INTRESOURCE
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
- IS_INTRESOURCE
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IS_INTRESOURCE macro


## -description


Determines whether a value is an integer identifier for a resource. 


## -parameters




### -param _r

The pointer to be tested whether it contains an integer resource identifier. 


## -remarks



This macro checks whether all bits except the least 16 bits are zero. When true, <i>p</i> is an integer identifier for a resource. Otherwise it is typically a pointer to a string.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/menurc/resources">Resources Overview</a>
 

 

