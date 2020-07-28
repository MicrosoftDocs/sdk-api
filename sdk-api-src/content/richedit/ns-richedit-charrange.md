---
UID: NS:richedit._charrange
title: CHARRANGE (richedit.h)
description: Specifies a range of characters in a rich edit control.If the cpMin and cpMax members are equal, the range is empty. The range includes everything if cpMin is 0 and cpMax is �1.
helpviewer_keywords: ["CHARRANGE","CHARRANGE structure [Windows Controls]","_win32_CHARRANGE_str","_win32_CHARRANGE_str_cpp","controls.CHARRANGE","controls._win32_CHARRANGE_str","richedit/CHARRANGE"]
old-location: controls\CHARRANGE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\charrange.htm
ms.date: 12/05/2018
ms.keywords: CHARRANGE, CHARRANGE structure [Windows Controls], _win32_CHARRANGE_str, _win32_CHARRANGE_str_cpp, controls.CHARRANGE, controls._win32_CHARRANGE_str, richedit/CHARRANGE
f1_keywords:
- richedit/CHARRANGE
dev_langs:
- c++
req.header: richedit.h
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
- Richedit.h
api_name:
- CHARRANGE
targetos: Windows
req.typenames: CHARRANGE
req.redist: 
ms.custom: 19H1
---

# CHARRANGE structure


## -description


Specifies a range of characters in a rich edit control.

If the <b>cpMin</b> and <b>cpMax</b> members are equal, the range is empty. The range includes everything if <b>cpMin</b> is 0 and <b>cpMax</b> is –1.


## -struct-fields




### -field cpMin

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Character position index immediately preceding the first character in the range. 


### -field cpMax

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Character position immediately following the last character in the range. 


## -see-also




<a href="https://msdn.microsoft.com/60fcf13e-6c45-4f4e-9b54-70f0985122fb">EM_EXGETSEL</a>



<a href="https://msdn.microsoft.com/85a0d1d4-1826-4ac5-b823-de81a051441d">EM_EXSETSEL</a>



<b>Reference</b>
 

 

