---
UID: NS:richedit._repastespecial
title: REPASTESPECIAL (richedit.h)
description: Contains information identifying whether the display aspect of a pasted object should be based on the content of the object or the icon that represent the object.
helpviewer_keywords: ["DVASPECT_CONTENT","DVASPECT_ICON","REPASTESPECIAL","REPASTESPECIAL structure [Windows Controls]","_win32_REPASTESPECIAL_str","_win32_REPASTESPECIAL_str_cpp","controls.REPASTESPECIAL","controls._win32_REPASTESPECIAL_str","richedit/REPASTESPECIAL"]
old-location: controls\REPASTESPECIAL.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\repastespecial.htm
ms.date: 12/05/2018
ms.keywords: DVASPECT_CONTENT, DVASPECT_ICON, REPASTESPECIAL, REPASTESPECIAL structure [Windows Controls], _win32_REPASTESPECIAL_str, _win32_REPASTESPECIAL_str_cpp, controls.REPASTESPECIAL, controls._win32_REPASTESPECIAL_str, richedit/REPASTESPECIAL
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
targetos: Windows
req.typenames: REPASTESPECIAL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _repastespecial
 - richedit/_repastespecial
 - REPASTESPECIAL
 - richedit/REPASTESPECIAL
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
 - REPASTESPECIAL
---

# REPASTESPECIAL structure


## -description

Contains information identifying whether the display aspect of a pasted object should be based on the content of the object or the icon that represent the object.

## -struct-fields

### -field dwAspect

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Display aspect. It can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DVASPECT_CONTENT"></a><a id="dvaspect_content"></a><dl>
<dt><b>DVASPECT_CONTENT</b></dt>
</dl>
</td>
<td width="60%">
Aspect is based on the content of the object.

</td>
</tr>
<tr>
<td width="40%"><a id="DVASPECT_ICON"></a><a id="dvaspect_icon"></a><dl>
<dt><b>DVASPECT_ICON</b></dt>
</dl>
</td>
<td width="60%">
Aspect is based on the icon view of the object.

</td>
</tr>
</table>

### -field dwParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD_PTR</a></b>

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Aspect data. If <b>dwAspect</b> is DVASPECT_ICON, this member contains the handle to the metafile with the icon view of the object.

## -see-also

<a href="/windows/win32/controls/em-pastespecial">EM_PASTESPECIAL</a>