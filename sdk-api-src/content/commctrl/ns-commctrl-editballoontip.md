---
UID: NS:commctrl._tagEDITBALLOONTIP
title: EDITBALLOONTIP (commctrl.h)
description: Contains information about a balloon tip associated with a button control.
helpviewer_keywords: ["*PEDITBALLOONTIP","EDITBALLOONTIP","EDITBALLOONTIP structure [Windows Controls]","PEDITBALLOONTIP","PEDITBALLOONTIP structure pointer [Windows Controls]","TTI_ERROR","TTI_ERROR_LARGE","TTI_INFO","TTI_INFO_LARGE","TTI_NONE","TTI_WARNING","TTI_WARNING_LARGE","_win32_EDITBALLOONTIP_str","_win32_EDITBALLOONTIP_str_cpp","commctrl/EDITBALLOONTIP","commctrl/PEDITBALLOONTIP","controls.EDITBALLOONTIP","controls._win32_EDITBALLOONTIP_str"]
old-location: controls\EDITBALLOONTIP.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolstructures\editballoontip.htm
ms.date: 12/05/2018
ms.keywords: '*PEDITBALLOONTIP, EDITBALLOONTIP, EDITBALLOONTIP structure [Windows Controls], PEDITBALLOONTIP, PEDITBALLOONTIP structure pointer [Windows Controls], TTI_ERROR, TTI_ERROR_LARGE, TTI_INFO, TTI_INFO_LARGE, TTI_NONE, TTI_WARNING, TTI_WARNING_LARGE, _win32_EDITBALLOONTIP_str, _win32_EDITBALLOONTIP_str_cpp, commctrl/EDITBALLOONTIP, commctrl/PEDITBALLOONTIP, controls.EDITBALLOONTIP, controls._win32_EDITBALLOONTIP_str'
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
req.typenames: EDITBALLOONTIP, *PEDITBALLOONTIP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagEDITBALLOONTIP
 - commctrl/_tagEDITBALLOONTIP
 - PEDITBALLOONTIP
 - commctrl/PEDITBALLOONTIP
 - EDITBALLOONTIP
 - commctrl/EDITBALLOONTIP
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
 - EDITBALLOONTIP
---

# EDITBALLOONTIP structure


## -description

Contains information about a balloon tip associated with a button control.

## -struct-fields

### -field cbStruct

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A <b>DWORD</b> that contains the size, in bytes, of the structure.

### -field pszTitle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

A pointer to a Unicode string that contains the title of the balloon tip.

### -field pszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

A pointer to a Unicode string that contains the balloon tip text.

### -field ttiIcon

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

A value of type <b>INT</b> that specifies the type of icon to associate with the balloon tip. This member can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TTI_ERROR"></a><a id="tti_error"></a><dl>
<dt><b>TTI_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Use the error icon.

</td>
</tr>
<tr>
<td width="40%"><a id="TTI_INFO"></a><a id="tti_info"></a><dl>
<dt><b>TTI_INFO</b></dt>
</dl>
</td>
<td width="60%">
Use the information icon.

</td>
</tr>
<tr>
<td width="40%"><a id="TTI_NONE"></a><a id="tti_none"></a><dl>
<dt><b>TTI_NONE</b></dt>
</dl>
</td>
<td width="60%">
Use no icon.

</td>
</tr>
<tr>
<td width="40%"><a id="TTI_WARNING"></a><a id="tti_warning"></a><dl>
<dt><b>TTI_WARNING</b></dt>
</dl>
</td>
<td width="60%">
Use the warning icon.

</td>
</tr>
<tr>
<td width="40%"><a id="TTI_INFO_LARGE"></a><a id="tti_info_large"></a><dl>
<dt><b>TTI_INFO_LARGE</b></dt>
</dl>
</td>
<td width="60%">
Use the large information icon. This is assumed to be an HICON value.

</td>
</tr>
<tr>
<td width="40%"><a id="TTI_WARNING_LARGE"></a><a id="tti_warning_large"></a><dl>
<dt><b>TTI_WARNING_LARGE</b></dt>
</dl>
</td>
<td width="60%">
Use the large warning icon. This is assumed to be an HICON value.

</td>
</tr>
<tr>
<td width="40%"><a id="TTI_ERROR_LARGE"></a><a id="tti_error_large"></a><dl>
<dt><b>TTI_ERROR_LARGE</b></dt>
</dl>
</td>
<td width="60%">
Use the large error icon. This is assumed to be an HICON value.

</td>
</tr>
</table>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/Controls/em-showballoontip">EM_SHOWBALLOONTIP</a>



<a href="/windows/desktop/Controls/edit-controls">Edit Controls</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-edit_showballoontip">Edit_ShowBalloonTip</a>



<b>Reference</b>