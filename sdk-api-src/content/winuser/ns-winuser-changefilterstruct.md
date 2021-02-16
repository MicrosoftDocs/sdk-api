---
UID: NS:winuser.tagCHANGEFILTERSTRUCT
title: CHANGEFILTERSTRUCT (winuser.h)
description: Contains extended result information obtained by calling the ChangeWindowMessageFilterEx function.
helpviewer_keywords: ["*PCHANGEFILTERSTRUCT","CHANGEFILTERSTRUCT","CHANGEFILTERSTRUCT structure [Windows and Messages]","MSGFLTINFO_ALLOWED_HIGHER","MSGFLTINFO_ALREADYALLOWED_FORWND","MSGFLTINFO_ALREADYDISALLOWED_FORWND","MSGFLTINFO_NONE","PCHANGEFILTERSTRUCT","PCHANGEFILTERSTRUCT structure pointer [Windows and Messages]","_win32_CHANGEFILTERSTRUCT_str","_win32_changefilterstruct_str_cpp","winmsg.changefilterstruct","winui._win32_changefilterstruct_str","winuser/CHANGEFILTERSTRUCT","winuser/PCHANGEFILTERSTRUCT"]
old-location: winmsg\changefilterstruct.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowstructures\changefilterstruct.htm
ms.date: 12/05/2018
ms.keywords: '*PCHANGEFILTERSTRUCT, CHANGEFILTERSTRUCT, CHANGEFILTERSTRUCT structure [Windows and Messages], MSGFLTINFO_ALLOWED_HIGHER, MSGFLTINFO_ALREADYALLOWED_FORWND, MSGFLTINFO_ALREADYDISALLOWED_FORWND, MSGFLTINFO_NONE, PCHANGEFILTERSTRUCT, PCHANGEFILTERSTRUCT structure pointer [Windows and Messages], _win32_CHANGEFILTERSTRUCT_str, _win32_changefilterstruct_str_cpp, winmsg.changefilterstruct, winui._win32_changefilterstruct_str, winuser/CHANGEFILTERSTRUCT, winuser/PCHANGEFILTERSTRUCT'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: CHANGEFILTERSTRUCT, *PCHANGEFILTERSTRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCHANGEFILTERSTRUCT
 - winuser/tagCHANGEFILTERSTRUCT
 - PCHANGEFILTERSTRUCT
 - winuser/PCHANGEFILTERSTRUCT
 - CHANGEFILTERSTRUCT
 - winuser/CHANGEFILTERSTRUCT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - CHANGEFILTERSTRUCT
---

# CHANGEFILTERSTRUCT structure


## -description

Contains extended result information obtained by calling
			the <a href="/windows/desktop/api/winuser/nf-winuser-changewindowmessagefilterex">ChangeWindowMessageFilterEx</a> function.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size of the structure, in bytes. 
				Must be set to <code>sizeof(CHANGEFILTERSTRUCT)</code>, otherwise the function fails with <b>ERROR_INVALID_PARAMETER</b>.

### -field ExtStatus

Type: <b>DWORD</b>

If the function succeeds, this field contains one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSGFLTINFO_NONE"></a><a id="msgfltinfo_none"></a><dl>
<dt><b>MSGFLTINFO_NONE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
See the Remarks section.
						Applies to <b>MSGFLT_ALLOW</b> and <b>MSGFLT_DISALLOW</b>.
					

</td>
</tr>
<tr>
<td width="40%"><a id="MSGFLTINFO_ALLOWED_HIGHER"></a><a id="msgfltinfo_allowed_higher"></a><dl>
<dt><b>MSGFLTINFO_ALLOWED_HIGHER</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The message is allowed at a scope
					 higher than the window. Applies to <b>MSGFLT_DISALLOW</b>. 

</td>
</tr>
<tr>
<td width="40%"><a id="MSGFLTINFO_ALREADYALLOWED_FORWND"></a><a id="msgfltinfo_alreadyallowed_forwnd"></a><dl>
<dt><b>MSGFLTINFO_ALREADYALLOWED_FORWND</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The message has already 
					been allowed by this window's message filter, and 
					the function thus succeeded with no change to the window's message filter.
					Applies to <b>MSGFLT_ALLOW</b>. 

</td>
</tr>
<tr>
<td width="40%"><a id="MSGFLTINFO_ALREADYDISALLOWED_FORWND"></a><a id="msgfltinfo_alreadydisallowed_forwnd"></a><dl>
<dt><b>MSGFLTINFO_ALREADYDISALLOWED_FORWND</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The message 
					has already been blocked by this window's message filter, and the function thus succeeded with no change to the window's message filter.
					Applies to <b>MSGFLT_DISALLOW</b>. 

</td>
</tr>
</table>

## -remarks

Certain messages whose value is smaller than <b>WM_USER</b> are required to pass through the filter, 
		regardless of the filter setting. There will be no effect when you attempt to use this function to allow or 
		block such messages.
		

An application may use the <a href="/windows/desktop/api/winuser/nf-winuser-changewindowmessagefilter">ChangeWindowMessageFilter</a> function to 
		allow or block a message in a process-wide manner. 
		If the message is allowed by either the process message filter 
		or the window message filter, it will be delivered to the window.
		

The following table lists the possible values returned in <b>ExtStatus</b>.

<table>
<tr>
<th>Message already allowed at higher scope</th>
<th>Message already allowed by window's message filter</th>
<th>Operation requested</th>
<th>Indicator returned in ExtStatus on success</th>
</tr>
<tr>
<td>No</td>
<td>No</td>
<td><b>MSGFLT_ALLOW</b></td>
<td><b>MSGFLTINFO_NONE</b></td>
</tr>
<tr>
<td>No</td>
<td>No</td>
<td><b>MSGFLT_DISALLOW</b></td>
<td><b>MSGFLTINFO_ALREADYDISALLOWED_FORWND</b></td>
</tr>
<tr>
<td>No</td>
<td>No</td>
<td><b>MSGFLT_RESET</b></td>
<td><b>MSGFLTINFO_NONE</b></td>
</tr>
<tr>
<td>No</td>
<td>Yes</td>
<td><b>MSGFLT_ALLOW</b></td>
<td><b>MSGFLTINFO_ALREADYALLOWED_FORWND</b></td>
</tr>
<tr>
<td>No</td>
<td>Yes</td>
<td><b>MSGFLT_DISALLOW</b></td>
<td><b>MSGFLTINFO_NONE</b></td>
</tr>
<tr>
<td>No</td>
<td>Yes</td>
<td><b>MSGFLT_RESET</b></td>
<td><b>MSGFLTINFO_NONE</b></td>
</tr>
<tr>
<td>Yes</td>
<td>No</td>
<td><b>MSGFLT_ALLOW</b></td>
<td><b>MSGFLTINFO_NONE</b></td>
</tr>
<tr>
<td>Yes</td>
<td>No</td>
<td><b>MSGFLT_DISALLOW</b></td>
<td><b>MSGFLTINFO_ALLOWED_HIGHER</b></td>
</tr>
<tr>
<td>Yes</td>
<td>No</td>
<td><b>MSGFLT_RESET</b></td>
<td><b>MSGFLTINFO_NONE</b></td>
</tr>
<tr>
<td>Yes</td>
<td>Yes</td>
<td><b>MSGFLT_ALLOW</b></td>
<td><b>MSGFLTINFO_ALREADYALLOWED_FORWND</b></td>
</tr>
<tr>
<td>Yes</td>
<td>Yes</td>
<td><b>MSGFLT_DISALLOW</b></td>
<td><b>MSGFLTINFO_ALLOWED_HIGHER</b></td>
</tr>
<tr>
<td>Yes</td>
<td>Yes</td>
<td><b>MSGFLT_RESET</b></td>
<td><b>MSGFLTINFO_NONE</b></td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-changewindowmessagefilterex">ChangeWindowMessageFilterEx</a>