---
UID: NS:richedit._textrange
title: "_textrange"
author: windows-sdk-content
description: A range of text from a rich edit control. This structure is filled in by the EM_GETTEXTRANGE message. The buffer pointed to by the lpstrText member must be large enough to receive all characters and the terminating null character.
old-location: controls\TEXTRANGE.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\textrange.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: TEXTRANGE, TEXTRANGE structure [Windows Controls], TEXTRANGEA, TEXTRANGEW, _textrange, _win32_TEXTRANGE_str, _win32_TEXTRANGE_str_cpp, controls.TEXTRANGE, controls._win32_TEXTRANGE_str, richedit/TEXTRANGE, richedit/TEXTRANGEA, richedit/TEXTRANGEW
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
req.unicode-ansi: TEXTRANGEW (Unicode) and TEXTRANGEA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TEXTRANGEA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - TEXTRANGE
 - TEXTRANGEA
 - TEXTRANGEW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _textrange structure


## -description


A range of text from a rich edit control. This structure is filled in by the <a href="https://msdn.microsoft.com/18398963-eb2c-4f64-99f5-9614a5d34b52">EM_GETTEXTRANGE</a> message. The buffer pointed to by the <b>lpstrText</b> member must be large enough to receive all characters and the terminating null character.


## -struct-fields




### -field chrg

Type: <b><a href="https://msdn.microsoft.com/144aadcb-92c9-408b-b2ae-a0a4e12c4759">CHARRANGE</a></b>

The range of characters to retrieve. 


### -field lpstrText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPSTR</a></b>

The text. 


## -see-also




<a href="https://msdn.microsoft.com/144aadcb-92c9-408b-b2ae-a0a4e12c4759">CHARRANGE</a>



<a href="https://msdn.microsoft.com/18398963-eb2c-4f64-99f5-9614a5d34b52">EM_GETTEXTRANGE</a>



<b>Reference</b>
 

 

