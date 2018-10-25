---
UID: NS:richedit._compcolor
title: "_compcolor"
author: windows-sdk-content
description: Contains color settings for a composition string.
old-location: controls\COMPCOLOR.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\compcolor.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: COMPCOLOR, COMPCOLOR structure [Windows Controls], _compcolor, _win32_COMPCOLOR_str, _win32_COMPCOLOR_str_cpp, controls.COMPCOLOR, controls._win32_COMPCOLOR_str, richedit/COMPCOLOR
ms.prod: windows
ms.technology: windows-sdk
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
 - COMPCOLOR
product: Windows
targetos: Windows
req.typenames: COMPCOLOR
req.redist: 
---

# _compcolor structure


## -description


Contains color settings for a composition string.


## -struct-fields




### -field crText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

Color of text. To generate a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro. 


### -field crBackground

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

Color of background. To generate a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro. 


### -field dwEffects

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Character effect values as described for the 
					<b>dwEffects</b> member in the <a href="https://msdn.microsoft.com/en-us/library/Bb787881(v=VS.85).aspx">CHARFORMAT</a> structure. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb787881(v=VS.85).aspx">CHARFORMAT</a>



<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>



<b>Reference</b>
 

 

