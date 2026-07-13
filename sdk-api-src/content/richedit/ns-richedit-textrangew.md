---
UID: NS:richedit._textrangew
title: TEXTRANGEW (richedit.h)
description: A range of text from a rich edit control. This structure is filled in by the EM_GETTEXTRANGE message. The buffer pointed to by the lpstrText member must be large enough to receive all characters and the terminating null character. (Unicode)
helpviewer_keywords: ["TEXTRANGE","TEXTRANGE structure [Windows Controls]","TEXTRANGEA","TEXTRANGEW","_win32_TEXTRANGE_str","_win32_TEXTRANGE_str_cpp","controls.TEXTRANGE","controls._win32_TEXTRANGE_str","richedit/TEXTRANGE","richedit/TEXTRANGEA","richedit/TEXTRANGEW"]
old-location: controls\TEXTRANGE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\textrange.htm
ms.date: 12/05/2018
ms.keywords: TEXTRANGE, TEXTRANGE structure [Windows Controls], TEXTRANGEA, TEXTRANGEW, _win32_TEXTRANGE_str, _win32_TEXTRANGE_str_cpp, controls.TEXTRANGE, controls._win32_TEXTRANGE_str, richedit/TEXTRANGE, richedit/TEXTRANGEA, richedit/TEXTRANGEW
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TEXTRANGEW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _textrangew
 - richedit/_textrangew
 - TEXTRANGEW
 - richedit/TEXTRANGEW
dev_langs:
 - c++
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
---

# TEXTRANGEW structure


## -description

A range of text from a rich edit control. This structure is filled in by the <a href="/windows/win32/controls/em-gettextrange">EM_GETTEXTRANGE</a> message. The buffer pointed to by the <b>lpstrText</b> member must be large enough to receive all characters and the terminating null character.

## -struct-fields

### -field chrg

Type: <b><a href="/windows/win32/api/richedit/ns-richedit-charrange">CHARRANGE</a></b>

The range of characters to retrieve.

### -field lpstrText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPSTR</a></b>

The text.

## -see-also

<a href="/windows/win32/api/richedit/ns-richedit-charrange">CHARRANGE</a>



<a href="/windows/win32/controls/em-gettextrange">EM_GETTEXTRANGE</a>



<b>Reference</b>

## -remarks

> [!NOTE]
> The richedit.h header defines TEXTRANGE as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
