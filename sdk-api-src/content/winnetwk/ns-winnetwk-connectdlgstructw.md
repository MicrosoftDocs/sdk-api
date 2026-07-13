---
UID: NS:winnetwk._CONNECTDLGSTRUCTW
title: CONNECTDLGSTRUCTW (winnetwk.h)
description: Used by the WNetConnectionDialog1 function to establish browsing dialog box parameters. (Unicode)
helpviewer_keywords: ["*LPCONNECTDLGSTRUCTW","CONNDLG_CONN_POINT","CONNDLG_HIDE_BOX","CONNDLG_NOT_PERSIST","CONNDLG_PERSIST","CONNDLG_RO_PATH","CONNDLG_USE_MRU","CONNECTDLGSTRUCT","CONNECTDLGSTRUCT structure [Windows Networking (WNet)]","CONNECTDLGSTRUCTA","CONNECTDLGSTRUCTW","LPCONNECTDLGSTRUCT","LPCONNECTDLGSTRUCT structure pointer [Windows Networking (WNet)]","SidTypeUser","_win32_connectdlgstruct_str","winnetwk/CONNECTDLGSTRUCT","winnetwk/CONNECTDLGSTRUCTA","winnetwk/CONNECTDLGSTRUCTW","winnetwk/LPCONNECTDLGSTRUCT","wnet.connectdlgstruct_str"]
old-location: wnet\connectdlgstruct_str.htm
tech.root: WNet
ms.assetid: fb2a4b5a-ad8a-4ebf-8430-349d821eee20
ms.date: 12/05/2018
ms.keywords: '*LPCONNECTDLGSTRUCTW, CONNDLG_CONN_POINT, CONNDLG_HIDE_BOX, CONNDLG_NOT_PERSIST, CONNDLG_PERSIST, CONNDLG_RO_PATH, CONNDLG_USE_MRU, CONNECTDLGSTRUCT, CONNECTDLGSTRUCT structure [Windows Networking (WNet)], CONNECTDLGSTRUCTA, CONNECTDLGSTRUCTW, LPCONNECTDLGSTRUCT, LPCONNECTDLGSTRUCT structure pointer [Windows Networking (WNet)], SidTypeUser, _win32_connectdlgstruct_str, winnetwk/CONNECTDLGSTRUCT, winnetwk/CONNECTDLGSTRUCTA, winnetwk/CONNECTDLGSTRUCTW, winnetwk/LPCONNECTDLGSTRUCT, wnet.connectdlgstruct_str'
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CONNECTDLGSTRUCTW (Unicode) and CONNECTDLGSTRUCTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CONNECTDLGSTRUCTW, *LPCONNECTDLGSTRUCTW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CONNECTDLGSTRUCTW
 - winnetwk/_CONNECTDLGSTRUCTW
 - LPCONNECTDLGSTRUCTW
 - winnetwk/LPCONNECTDLGSTRUCTW
 - CONNECTDLGSTRUCTW
 - winnetwk/CONNECTDLGSTRUCTW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnetwk.h
api_name:
 - CONNECTDLGSTRUCT
 - CONNECTDLGSTRUCTA
 - CONNECTDLGSTRUCTW
---

# CONNECTDLGSTRUCTW structure


## -description

The
				<b>CONNECTDLGSTRUCT</b> structure is used by the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a">WNetConnectionDialog1</a> function to establish browsing dialog box parameters.

## -struct-fields

### -field cbStructure

Type: <b>DWORD</b>

The size, in bytes, of the 
<b>CONNECTDLGSTRUCT</b> structure. The caller must supply this value.

### -field hwndOwner

Type: <b>HWND</b>

The handle to the owner window for the dialog box.

### -field lpConnRes

Type: <b>LPNETRESOURCE</b>

A pointer to a <a href="ns-winnetwk-netresourcew.md">NETRESOURCE</a> structure. 




If the <b>lpRemoteName</b> member of 
<b>NETRESOURCE</b> is specified, it will be entered into the path field of the dialog box. With the exception of the <b>dwType</b> member, all other members of the 
<b>NETRESOURCE</b> structure must be set to <b>NULL</b>. The <b>dwType</b> member must be equal to RESOURCETYPE_DISK.
							

 The system does not support the <b>RESOURCETYPE_PRINT</b> flag for browsing and connecting to print resources.

### -field dwFlags

Type: <b>DWORD</b>

A set of bit flags that describe options for the dialog box display. This member can be a combination of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SidTypeUser"></a><a id="sidtypeuser"></a><a id="SIDTYPEUSER"></a><dl>
<dt><b>SidTypeUser</b></dt>
</dl>
</td>
<td width="60%">
The account is a user account.

</td>
</tr>
<tr>
<td width="40%"><a id="CONNDLG_RO_PATH"></a><a id="conndlg_ro_path"></a><dl>
<dt><b>CONNDLG_RO_PATH</b></dt>
</dl>
</td>
<td width="60%">
Display a read-only path instead of allowing the user to type in a path. 




This flag should be set only if the <b>lpRemoteName</b> member of the 
<a href="ns-winnetwk-netresourcew.md">NETRESOURCE</a> structure pointed to by <b>lpConnRes</b> member is not <b>NULL</b> (or an empty string), and the <b>CONNDLG_USE_MRU</b> flag is not set.

</td>
</tr>
<tr>
<td width="40%"><a id="CONNDLG_CONN_POINT"></a><a id="conndlg_conn_point"></a><dl>
<dt><b>CONNDLG_CONN_POINT</b></dt>
</dl>
</td>
<td width="60%">
Internal flag. Do not use.

</td>
</tr>
<tr>
<td width="40%"><a id="CONNDLG_USE_MRU"></a><a id="conndlg_use_mru"></a><dl>
<dt><b>CONNDLG_USE_MRU</b></dt>
</dl>
</td>
<td width="60%">
Enter the most recently used paths into the combination box. Set this value to simulate the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetconnectiondialog">WNetConnectionDialog</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CONNDLG_HIDE_BOX"></a><a id="conndlg_hide_box"></a><dl>
<dt><b>CONNDLG_HIDE_BOX</b></dt>
</dl>
</td>
<td width="60%">
Show the check box allowing the user to restore the connection at logon.

</td>
</tr>
<tr>
<td width="40%"><a id="CONNDLG_PERSIST"></a><a id="conndlg_persist"></a><dl>
<dt><b>CONNDLG_PERSIST</b></dt>
</dl>
</td>
<td width="60%">
Restore the connection at logon.

</td>
</tr>
<tr>
<td width="40%"><a id="CONNDLG_NOT_PERSIST"></a><a id="conndlg_not_persist"></a><dl>
<dt><b>CONNDLG_NOT_PERSIST</b></dt>
</dl>
</td>
<td width="60%">
Do not restore the connection at logon.

</td>
</tr>
</table>
 

For more information, see the following Remarks section.

### -field dwDevNum

Type: <b>DWORD</b>

If the call to the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a">WNetConnectionDialog1</a> function is successful, this member returns the number of the connected device. The value is 1 for A:, 2 for B:, 3 for C:, and so on. If the user made a deviceless connection, the value is –1.

## -remarks

If neither the CONNDLG_RO_PATH nor the CONNDLG_USE_MRU flag is set, and the <b>lpRemoteName</b> member of the 
<b>NETRESOURCE</b> structure does not specify a remote path, the request defaults to the CONNDLG_RO_PATH dialog display type.

The CONNDLG_PERSIST and CONNDLG_NOT_PERSIST values cannot both be set. If neither is set, the dialog box defaults to the last option that was selected in this dialog box for the particular type of device connection.





> [!NOTE]
> The winnetwk.h header defines CONNECTDLGSTRUCT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="ns-winnetwk-netresourcew.md">NETRESOURCE</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a">WNetConnectionDialog1</a>



<a href="/windows/desktop/WNet/windows-networking-wnet-">Windows Networking (WNet) Overview</a>



<a href="/windows/desktop/WNet/windows-networking-structures">Windows Networking Structures</a>
