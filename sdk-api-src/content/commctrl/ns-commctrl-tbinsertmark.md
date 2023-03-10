---
UID: NS:commctrl.TBINSERTMARK
title: TBINSERTMARK (commctrl.h)
description: Contains information on the insertion mark in a toolbar control.
helpviewer_keywords: ["*LPTBINSERTMARK","0","LPTBINSERTMARK","LPTBINSERTMARK structure pointer [Windows Controls]","TBIMHT_AFTER","TBIMHT_BACKGROUND","TBINSERTMARK","TBINSERTMARK structure [Windows Controls]","_win32_TBINSERTMARK","_win32_TBINSERTMARK_cpp","commctrl/LPTBINSERTMARK","commctrl/TBINSERTMARK","controls.TBINSERTMARK","controls._win32_TBINSERTMARK"]
old-location: controls\TBINSERTMARK.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\tbinsertmark.htm
ms.date: 12/05/2018
ms.keywords: '*LPTBINSERTMARK, 0, LPTBINSERTMARK, LPTBINSERTMARK structure pointer [Windows Controls], TBIMHT_AFTER, TBIMHT_BACKGROUND, TBINSERTMARK, TBINSERTMARK structure [Windows Controls], _win32_TBINSERTMARK, _win32_TBINSERTMARK_cpp, commctrl/LPTBINSERTMARK, commctrl/TBINSERTMARK, controls.TBINSERTMARK, controls._win32_TBINSERTMARK'
req.header: commctrl.h
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
req.typenames: TBINSERTMARK, *LPTBINSERTMARK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPTBINSERTMARK
 - commctrl/LPTBINSERTMARK
 - TBINSERTMARK
 - commctrl/TBINSERTMARK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TBINSERTMARK
---

# TBINSERTMARK structure


## -description

Contains information on the insertion mark in a toolbar control.

## -struct-fields

### -field iButton

Type: <b>int</b>

Zero-based index of the insertion mark. If this member is -1, there is no insertion mark.

### -field dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Defines where the insertion mark is in relation to 
					<b>iButton</b>. This can be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The insertion mark is to the left of the specified button. 

</td>
</tr>
<tr>
<td width="40%"><a id="TBIMHT_AFTER"></a><a id="tbimht_after"></a><dl>
<dt><b>TBIMHT_AFTER</b></dt>
</dl>
</td>
<td width="60%">
The insertion mark is to the right of the specified button. 

</td>
</tr>
<tr>
<td width="40%"><a id="TBIMHT_BACKGROUND"></a><a id="tbimht_background"></a><dl>
<dt><b>TBIMHT_BACKGROUND</b></dt>
</dl>
</td>
<td width="60%">
The insertion mark is on the background of the toolbar. This flag is only used with the <a href="/windows/desktop/Controls/tb-insertmarkhittest">TB_INSERTMARKHITTEST</a> message. 

</td>
</tr>
</table>

