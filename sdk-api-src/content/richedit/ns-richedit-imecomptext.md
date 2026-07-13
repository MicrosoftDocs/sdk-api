---
UID: NS:richedit._imecomptext
title: IMECOMPTEXT (richedit.h)
description: Contains information about the Input Method Editor (IME) composition text in a Microsoft Rich Edit control.
helpviewer_keywords: ["ICT_RESULTREADSTR","IMECOMPTEXT","IMECOMPTEXT structure [Windows Controls]","_win32_IMECOMPTEXT_str","_win32_IMECOMPTEXT_str_cpp","controls.IMECOMPTEXT","controls._win32_IMECOMPTEXT_str","richedit/IMECOMPTEXT"]
old-location: controls\IMECOMPTEXT.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\imecomptext.htm
ms.date: 12/05/2018
ms.keywords: ICT_RESULTREADSTR, IMECOMPTEXT, IMECOMPTEXT structure [Windows Controls], _win32_IMECOMPTEXT_str, _win32_IMECOMPTEXT_str_cpp, controls.IMECOMPTEXT, controls._win32_IMECOMPTEXT_str, richedit/IMECOMPTEXT
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
targetos: Windows
req.typenames: IMECOMPTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _imecomptext
 - richedit/_imecomptext
 - IMECOMPTEXT
 - richedit/IMECOMPTEXT
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
 - IMECOMPTEXT
---

# IMECOMPTEXT structure


## -description

Contains information about the Input Method Editor (IME) composition text in a Microsoft Rich Edit control.

## -struct-fields

### -field cb

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Size of the output buffer, in bytes.

### -field flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Type of composition string. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ICT_RESULTREADSTR"></a><a id="ict_resultreadstr"></a><dl>
<dt><b>ICT_RESULTREADSTR</b></dt>
</dl>
</td>
<td width="60%">
The final composed string.

</td>
</tr>
</table>

## -remarks

This structure is used with the <a href="/windows/win32/controls/em-getimecomptext">EM_GETIMECOMPTEXT</a> message.

## -see-also

<a href="/windows/win32/controls/em-getimecomptext">EM_GETIMECOMPTEXT</a>