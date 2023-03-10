---
UID: NF:winuser.GetIconInfoExW
title: GetIconInfoExW function (winuser.h)
description: Retrieves information about the specified icon or cursor. GetIconInfoEx extends GetIconInfo by using the newer ICONINFOEX structure. (Unicode)
helpviewer_keywords: ["GetIconInfoEx", "GetIconInfoEx function [Menus and Other Resources]", "GetIconInfoExW", "IDC_APPSTARTING", "IDC_ARROW", "IDC_CROSS", "IDC_HAND", "IDC_HELP", "IDC_IBEAM", "IDC_NO", "IDC_SIZEALL", "IDC_SIZENESW", "IDC_SIZENS", "IDC_SIZENWSE", "IDC_SIZEWE", "IDC_UPARROW", "IDC_WAIT", "IDI_APPLICATION", "IDI_ASTERISK", "IDI_EXCLAMATION", "IDI_HAND", "IDI_QUESTION", "IDI_WINLOGO", "_win32_GetIconInfoEx", "_win32_geticoninfoex_cpp", "menurc.geticoninfoex", "winui._win32_geticoninfoex", "winuser/GetIconInfoEx", "winuser/GetIconInfoExW"]
old-location: menurc\geticoninfoex.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\geticoninfoex.htm
ms.date: 12/05/2018
ms.keywords: GetIconInfoEx, GetIconInfoEx function [Menus and Other Resources], GetIconInfoExA, GetIconInfoExW, IDC_APPSTARTING, IDC_ARROW, IDC_CROSS, IDC_HAND, IDC_HELP, IDC_IBEAM, IDC_NO, IDC_SIZEALL, IDC_SIZENESW, IDC_SIZENS, IDC_SIZENWSE, IDC_SIZEWE, IDC_UPARROW, IDC_WAIT, IDI_APPLICATION, IDI_ASTERISK, IDI_EXCLAMATION, IDI_HAND, IDI_QUESTION, IDI_WINLOGO, _win32_GetIconInfoEx, _win32_geticoninfoex_cpp, menurc.geticoninfoex, winui._win32_geticoninfoex, winuser/GetIconInfoEx, winuser/GetIconInfoExA, winuser/GetIconInfoExW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetIconInfoExW (Unicode) and GetIconInfoExA (ANSI)
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
 - GetIconInfoExW
 - winuser/GetIconInfoExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetIconInfoEx
 - GetIconInfoExA
 - GetIconInfoExW
---

# GetIconInfoExW function


## -description

Retrieves information about the specified icon or cursor. <b>GetIconInfoEx</b> extends <a href="/windows/desktop/api/winuser/nf-winuser-geticoninfo">GetIconInfo</a> by using the newer <a href="/windows/desktop/api/winuser/ns-winuser-iconinfoexa">ICONINFOEX</a> structure.

## -parameters

### -param hicon [in]

Type: <b>HICON</b>

A handle to the icon or cursor. To retrieve information about a standard icon or cursor, specify one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IDC_APPSTARTING"></a><a id="idc_appstarting"></a><dl>
<dt><b>IDC_APPSTARTING</b></dt>
<dt>MAKEINTRESOURCE(32650)</dt>
</dl>
</td>
<td width="60%">
Standard arrow and small hourglass cursor.

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_ARROW"></a><a id="idc_arrow"></a><dl>
<dt><b>IDC_ARROW</b></dt>
<dt>MAKEINTRESOURCE(32512)</dt>
</dl>
</td>
<td width="60%">
Standard arrow cursor.

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_CROSS"></a><a id="idc_cross"></a><dl>
<dt><b>IDC_CROSS</b></dt>
<dt>MAKEINTRESOURCE(32515)</dt>
</dl>
</td>
<td width="60%">
Crosshair cursor.

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_HAND"></a><a id="idc_hand"></a><dl>
<dt><b>IDC_HAND</b></dt>
<dt>MAKEINTRESOURCE(32649)</dt>
</dl>
</td>
<td width="60%">
 Hand cursor.

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_HELP"></a><a id="idc_help"></a><dl>
<dt><b>IDC_HELP</b></dt>
<dt>MAKEINTRESOURCE(32651)</dt>
</dl>
</td>
<td width="60%">
Arrow and question mark cursor.

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_IBEAM"></a><a id="idc_ibeam"></a><dl>
<dt><b>IDC_IBEAM</b></dt>
<dt>MAKEINTRESOURCE(32513)</dt>
</dl>
</td>
<td width="60%">
I-beam cursor.

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_NO"></a><a id="idc_no"></a><dl>
<dt><b>IDC_NO</b></dt>
<dt>MAKEINTRESOURCE(32648)</dt>
</dl>
</td>
<td width="60%">
Slashed circle cursor.

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_SIZEALL"></a><a id="idc_sizeall"></a><dl>
<dt><b>IDC_SIZEALL</b></dt>
<dt>MAKEINTRESOURCE(32646)</dt>
</dl>
</td>
<td width="60%">
Four-pointed arrow cursor pointing north, south, east, and west.

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_SIZENESW"></a><a id="idc_sizenesw"></a><dl>
<dt><b>IDC_SIZENESW</b></dt>
<dt>MAKEINTRESOURCE(32643)</dt>
</dl>
</td>
<td width="60%">
Double-pointed arrow cursor pointing northeast and southwest.

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_SIZENS"></a><a id="idc_sizens"></a><dl>
<dt><b>IDC_SIZENS</b></dt>
<dt>MAKEINTRESOURCE(32645)</dt>
</dl>
</td>
<td width="60%">
Double-pointed arrow cursor pointing north and south.

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_SIZENWSE"></a><a id="idc_sizenwse"></a><dl>
<dt><b>IDC_SIZENWSE</b></dt>
<dt>MAKEINTRESOURCE(32642)</dt>
</dl>
</td>
<td width="60%">
Double-pointed arrow cursor pointing northwest and southeast.

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_SIZEWE"></a><a id="idc_sizewe"></a><dl>
<dt><b>IDC_SIZEWE</b></dt>
<dt>MAKEINTRESOURCE(32644)</dt>
</dl>
</td>
<td width="60%">
Double-pointed arrow cursor pointing west and east.

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_UPARROW"></a><a id="idc_uparrow"></a><dl>
<dt><b>IDC_UPARROW</b></dt>
<dt>MAKEINTRESOURCE(32516)</dt>
</dl>
</td>
<td width="60%">
Vertical arrow cursor.

</td>
</tr>
<tr>
<td width="40%"><a id="IDC_WAIT"></a><a id="idc_wait"></a><dl>
<dt><b>IDC_WAIT</b></dt>
<dt>MAKEINTRESOURCE(32514)</dt>
</dl>
</td>
<td width="60%">
Hourglass cursor.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_APPLICATION"></a><a id="idi_application"></a><dl>
<dt><b>IDI_APPLICATION</b></dt>
<dt>MAKEINTRESOURCE(32512)</dt>
</dl>
</td>
<td width="60%">
Application icon.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_ASTERISK"></a><a id="idi_asterisk"></a><dl>
<dt><b>IDI_ASTERISK</b></dt>
<dt>MAKEINTRESOURCE(32516)</dt>
</dl>
</td>
<td width="60%">
Asterisk icon.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_EXCLAMATION"></a><a id="idi_exclamation"></a><dl>
<dt><b>IDI_EXCLAMATION</b></dt>
<dt>MAKEINTRESOURCE(32515)</dt>
</dl>
</td>
<td width="60%">
Exclamation point icon.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_HAND"></a><a id="idi_hand"></a><dl>
<dt><b>IDI_HAND</b></dt>
<dt>MAKEINTRESOURCE(32513)</dt>
</dl>
</td>
<td width="60%">
Stop sign icon.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_QUESTION"></a><a id="idi_question"></a><dl>
<dt><b>IDI_QUESTION</b></dt>
<dt>MAKEINTRESOURCE(32514)</dt>
</dl>
</td>
<td width="60%">
Question-mark icon.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_WINLOGO"></a><a id="idi_winlogo"></a><dl>
<dt><b>IDI_WINLOGO</b></dt>
<dt>MAKEINTRESOURCE(32517)</dt>
</dl>
</td>
<td width="60%">
 Application icon.

<b>Windows 2000:  </b>Windows logo icon. 

</td>
</tr>
</table>

### -param piconinfo [in, out]

Type: <b>PICONINFOEX</b>

When this method returns, contains a pointer to an <a href="/windows/desktop/api/winuser/ns-winuser-iconinfoexa">ICONINFOEX</a> structure. The function fills in the structure's members.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> indicates success, <b>FALSE</b> indicates failure.

## -remarks

<b>GetIconInfoEx</b> creates bitmaps for the <b>hbmMask</b> and <b>hbmColor</b> or members of <a href="/windows/desktop/api/winuser/ns-winuser-iconinfoexa">ICONINFOEX</a>. The calling application must manage these bitmaps and delete them when they are no longer necessary.

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The output returned is not affected by the DPI of the calling thread.

> [!NOTE]
> The winuser.h header defines GetIconInfoEx as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createicon">CreateIcon</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createiconfromresource">CreateIconFromResource</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createiconindirect">CreateIconIndirect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a>



<a href="/windows/desktop/api/winuser/nf-winuser-drawicon">DrawIcon</a>



<a href="/windows/desktop/api/winuser/nf-winuser-drawiconex">DrawIconEx</a>



<a href="/windows/desktop/api/winuser/ns-winuser-iconinfo">ICONINFO</a>



<a href="/windows/desktop/menurc/icons">Icons</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadicona">LoadIcon</a>



<a href="/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectory">LookupIconIdFromDirectory</a>



<b>Reference</b>
