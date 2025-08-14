---
UID: NF:winuser.GetScrollInfo
title: GetScrollInfo function (winuser.h)
description: The GetScrollInfo function retrieves the parameters of a scroll bar, including the minimum and maximum scrolling positions, the page size, and the position of the scroll box (thumb).
helpviewer_keywords: ["GetScrollInfo","GetScrollInfo function [Windows Controls]","SB_CTL","SB_HORZ","SB_VERT","SIF_PAGE","SIF_POS","SIF_RANGE","SIF_TRACKPOS","_win32_GetScrollInfo","_win32_GetScrollInfo_cpp","controls.GetScrollInfo","controls._win32_GetScrollInfo","winuser/GetScrollInfo"]
old-location: controls\GetScrollInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarfunctions\getscrollinfo.htm
ms.date: 12/05/2018
ms.keywords: GetScrollInfo, GetScrollInfo function [Windows Controls], SB_CTL, SB_HORZ, SB_VERT, SIF_PAGE, SIF_POS, SIF_RANGE, SIF_TRACKPOS, _win32_GetScrollInfo, _win32_GetScrollInfo_cpp, controls.GetScrollInfo, controls._win32_GetScrollInfo, winuser/GetScrollInfo
req.header: winuser.h
req.include-header: Windows.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetScrollInfo
 - winuser/GetScrollInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - GetScrollInfo
req.apiset: ext-ms-win-ntuser-misc-l1-2-0 (introduced in Windows 8.1)
---

# GetScrollInfo function


## -description

The <b>GetScrollInfo</b> function retrieves the parameters of a scroll bar, including the minimum and maximum scrolling positions, the page size, and the position of the scroll box (thumb).

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a scroll bar control or a window with a standard scroll bar, depending on the value of the 
					<i>fnBar</i> parameter.

### -param nBar [in]

Type: <b>int</b>

Specifies the type of scroll bar for which to retrieve parameters. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SB_CTL"></a><a id="sb_ctl"></a><dl>
<dt><b>SB_CTL</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the parameters for a scroll bar control. The 
						<i>hwnd</i> parameter must be the handle to the scroll bar control. 

</td>
</tr>
<tr>
<td width="40%"><a id="SB_HORZ"></a><a id="sb_horz"></a><dl>
<dt><b>SB_HORZ</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the parameters for the window's standard horizontal scroll bar. 

</td>
</tr>
<tr>
<td width="40%"><a id="SB_VERT"></a><a id="sb_vert"></a><dl>
<dt><b>SB_VERT</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the parameters for the window's standard vertical scroll bar. 

</td>
</tr>
</table>

### -param lpsi [in, out]

Type: <b>LPSCROLLINFO</b>

Pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-scrollinfo">SCROLLINFO</a> structure. Before calling <b>GetScrollInfo</b>, set the 
					<b>cbSize</b> member to 
					<b>sizeof</b>(<b>SCROLLINFO</b>), and set the 
					<b>fMask</b> member to specify the scroll bar parameters to retrieve. Before returning, the function copies the specified parameters to the appropriate members of the structure.

The 
					<b>fMask</b> member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SIF_PAGE"></a><a id="sif_page"></a><dl>
<dt><b>SIF_PAGE</b></dt>
</dl>
</td>
<td width="60%">
Copies the scroll page to the 
						<b>nPage</b> member of the <a href="/windows/desktop/api/winuser/ns-winuser-scrollinfo">SCROLLINFO</a> structure pointed to by 
						<i>lpsi</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="SIF_POS"></a><a id="sif_pos"></a><dl>
<dt><b>SIF_POS</b></dt>
</dl>
</td>
<td width="60%">
Copies the scroll position to the 
						<b>nPos</b> member of the <a href="/windows/desktop/api/winuser/ns-winuser-scrollinfo">SCROLLINFO</a> structure pointed to by 
						<i>lpsi</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="SIF_RANGE"></a><a id="sif_range"></a><dl>
<dt><b>SIF_RANGE</b></dt>
</dl>
</td>
<td width="60%">
Copies the scroll range to the 
						<b>nMin</b> and 
						<b>nMax</b> members of the <a href="/windows/desktop/api/winuser/ns-winuser-scrollinfo">SCROLLINFO</a> structure pointed to by 
						<i>lpsi</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="SIF_TRACKPOS"></a><a id="sif_trackpos"></a><dl>
<dt><b>SIF_TRACKPOS</b></dt>
</dl>
</td>
<td width="60%">
Copies the current scroll box tracking position to the 
						<b>nTrackPos</b> member of the <a href="/windows/desktop/api/winuser/ns-winuser-scrollinfo">SCROLLINFO</a> structure pointed to by 
						<i>lpsi</i>.

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If the function retrieved any values, the return value is nonzero.

If the function does not retrieve any values, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>GetScrollInfo</b> function enables applications to use 32-bit scroll positions. Although the messages that indicate scroll bar position, <a href="/windows/desktop/Controls/wm-hscroll">WM_HSCROLL</a> and <a href="/windows/desktop/Controls/wm-vscroll">WM_VSCROLL</a>, provide only 16 bits of position data, the functions <a href="/windows/desktop/api/winuser/nf-winuser-setscrollinfo">SetScrollInfo</a> and <b>GetScrollInfo</b> provide 32 bits of scroll bar position data. Thus, an application can call <b>GetScrollInfo</b> while processing either the <b>WM_HSCROLL</b> or <b>WM_VSCROLL</b> messages to obtain 32-bit scroll bar position data. 

To get the 32-bit position of the scroll box (thumb) during a SB_THUMBTRACK request code in a <a href="/windows/desktop/Controls/wm-hscroll">WM_HSCROLL</a> or <a href="/windows/desktop/Controls/wm-vscroll">WM_VSCROLL</a> message, call <b>GetScrollInfo</b> with the SIF_TRACKPOS value in the 
				<b>fMask</b> member of the <a href="/windows/desktop/api/winuser/ns-winuser-scrollinfo">SCROLLINFO</a> structure. The function returns the tracking position of the scroll box in the 
				<b>nTrackPos</b> member of the <b>SCROLLINFO</b> structure. This allows you to get the position of the scroll box as the user moves it. The following sample code illustrates the technique.


```
SCROLLINFO si;
case WM_HSCROLL:
    switch(LOWORD(wparam)) {
        case SB_THUMBTRACK:
          // Initialize SCROLLINFO structure
 
            ZeroMemory(&si, sizeof(si));
            si.cbSize = sizeof(si);
            si.fMask = SIF_TRACKPOS;
 
          // Call GetScrollInfo to get current tracking 
          //    position in si.nTrackPos
 
            if (!GetScrollInfo(hwnd, SB_HORZ, &si) )
                return 1; // GetScrollInfo failed
            break;
        .
        .
        .
    }
```


If the <i>fnBar</i> parameter is SB_CTL and the window specified by the <i>hwnd</i> parameter is not a system scroll bar control, the system sends the <a href="/windows/desktop/Controls/sbm-getscrollinfo">SBM_GETSCROLLINFO</a> message to the window to obtain scroll bar information. This allows <b>GetScrollInfo</b> to operate on a custom control that mimics a scroll bar. If the window does not handle the <b>SBM_GETSCROLLINFO</b> message, the <b>GetScrollInfo</b> function fails.

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/winuser/ns-winuser-scrollinfo">SCROLLINFO</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setscrollinfo">SetScrollInfo</a>



<a href="/windows/desktop/Controls/wm-hscroll">WM_HSCROLL</a>



<a href="/windows/desktop/Controls/wm-vscroll">WM_VSCROLL</a>
