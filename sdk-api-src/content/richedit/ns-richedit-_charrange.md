---
UID: NS:richedit._charrange
title: "_charrange"
author: windows-sdk-content
description: Specifies a range of characters in a rich edit control.If the cpMin and cpMax members are equal, the range is empty. The range includes everything if cpMin is 0 and cpMax is &#8211;1.
old-location: controls\CHARRANGE.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\charrange.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CHARRANGE, CHARRANGE structure [Windows Controls], _charrange, _win32_CHARRANGE_str, _win32_CHARRANGE_str_cpp, controls.CHARRANGE, controls._win32_CHARRANGE_str, richedit/CHARRANGE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: CHARRANGE
req.redist: 
---

# _charrange structure


## -description


Specifies a range of characters in a rich edit control.

If the <b>cpMin</b> and <b>cpMax</b> members are equal, the range is empty. The range includes everything if <b>cpMin</b> is 0 and <b>cpMax</b> is –1.


## -struct-fields




### -field cpMin

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Character position index immediately preceding the first character in the range. 


### -field cpMax

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Character position immediately following the last character in the range. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb788001(v=VS.85).aspx">EM_EXGETSEL</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb788007(v=VS.85).aspx">EM_EXSETSEL</a>



<b>Reference</b>
 

 

