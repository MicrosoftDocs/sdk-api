---
UID: NS:richedit._compcolor
title: COMPCOLOR (richedit.h)
author: windows-sdk-content
description: Contains color settings for a composition string.
old-location: controls\COMPCOLOR.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\compcolor.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: COMPCOLOR, COMPCOLOR structure [Windows Controls], _win32_COMPCOLOR_str, _win32_COMPCOLOR_str_cpp, controls.COMPCOLOR, controls._win32_COMPCOLOR_str, richedit/COMPCOLOR
ms.topic: struct
f1_keywords: 
 - "richedit/COMPCOLOR"
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
 - COMPCOLOR
targetos: Windows
req.typenames: COMPCOLOR
req.redist: 
ms.custom: 19H1
---

# COMPCOLOR structure


## -description


Contains color settings for a composition string.


## -struct-fields




### -field crText

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

Color of text. To generate a <a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a>, use the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro. 


### -field crBackground

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

Color of background. To generate a <a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a>, use the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro. 


### -field dwEffects

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Character effect values as described for the 
					<b>dwEffects</b> member in the <a href="https://msdn.microsoft.com/7b31e42a-5e9b-46bf-9c4e-fd223c34a076">CHARFORMAT</a> structure. 


## -see-also




<a href="https://msdn.microsoft.com/7b31e42a-5e9b-46bf-9c4e-fd223c34a076">CHARFORMAT</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a>



<b>Other Resources</b>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>



<b>Reference</b>
 

 

