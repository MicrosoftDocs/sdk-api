---
UID: NF:winuser.MAKELPARAM
title: MAKELPARAM macro (winuser.h)
description: Creates a value for use as an lParam parameter in a message. The macro concatenates the specified values.helpviewer_keywords: ["MAKELPARAM","MAKELPARAM macro [Windows and Messages]","_win32_MAKELPARAM","_win32_makelparam_cpp","winmsg.makelparam","winui._win32_makelparam","winuser/MAKELPARAM"]
old-location: winmsg\makelparam.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmacros\makelparam.htm
ms.date: 12/05/2018
ms.keywords: MAKELPARAM, MAKELPARAM macro [Windows and Messages], _win32_MAKELPARAM, _win32_makelparam_cpp, winmsg.makelparam, winui._win32_makelparam, winuser/MAKELPARAM
f1_keywords:
- winuser/MAKELPARAM
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
- MAKELPARAM
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MAKELPARAM macro


## -description


Creates a value for use as an
			<i>lParam</i> parameter in a message. The macro concatenates the specified values. 


## -parameters




### -param l

The low-order word of the new value. 


### -param h

The high-order word of the new value. 


## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms632660(v=vs.85)">MAKELONG</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-makelresult">MAKELRESULT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-makewparam">MAKEWPARAM</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">Windows Data Types</a>
 

 

