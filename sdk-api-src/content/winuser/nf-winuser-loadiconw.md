---
UID: NF:winuser.LoadIconW
title: LoadIconW function (winuser.h)
description: Loads the specified icon resource from the executable (.exe) file associated with an application instance.
helpviewer_keywords: ["IDI_APPLICATION","IDI_ASTERISK","IDI_ERROR","IDI_EXCLAMATION","IDI_HAND","IDI_INFORMATION","IDI_QUESTION","IDI_SHIELD","IDI_WARNING","IDI_WINLOGO","LoadIcon","LoadIcon function [Menus and Other Resources]","LoadIconA","LoadIconW","_win32_LoadIcon","_win32_loadicon_cpp","menurc.loadicon","winui._win32_loadicon","winuser/LoadIcon","winuser/LoadIconA","winuser/LoadIconW"]
old-location: menurc\loadicon.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\loadicon.htm
ms.date: 12/05/2018
ms.keywords: IDI_APPLICATION, IDI_ASTERISK, IDI_ERROR, IDI_EXCLAMATION, IDI_HAND, IDI_INFORMATION, IDI_QUESTION, IDI_SHIELD, IDI_WARNING, IDI_WINLOGO, LoadIcon, LoadIcon function [Menus and Other Resources], LoadIconA, LoadIconW, _win32_LoadIcon, _win32_loadicon_cpp, menurc.loadicon, winui._win32_loadicon, winuser/LoadIcon, winuser/LoadIconA, winuser/LoadIconW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadIconW (Unicode) and LoadIconA (ANSI)
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
 - LoadIconW
 - winuser/LoadIconW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-0.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-GUI-l1-2-0.dll
 - api-ms-win-ntuser-ie-gui-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-NTUser-Gui-L1-3-0.dll
api_name:
 - LoadIcon
 - LoadIconA
 - LoadIconW
req.apiset: ext-ms-win-ntuser-gui-l1-1-0 (introduced in Windows 8)
---

# LoadIconW function


## -description

Loads the specified icon resource from the executable (.exe) file associated with an application instance.
<div class="alert"><b>Note</b>  This function has been superseded by the <a href="/windows/desktop/api/winuser/nf-winuser-loadimagea">LoadImage</a> function.</div><div> </div>

## -parameters

### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to an instance of the module whose executable file contains the icon to be loaded. This parameter must be <b>NULL</b> when a standard icon is being loaded.

### -param lpIconName [in]

Type: <b>LPCTSTR</b>

The name of the icon resource to be loaded. Alternatively, this parameter can contain the resource identifier in the low-order word and zero in the high-order word. Use the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro to create this value.

To use one of the predefined icons, set the <i>hInstance</i> parameter to <b>NULL</b> and the <i>lpIconName</i> parameter to one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IDI_APPLICATION"></a><a id="idi_application"></a><dl>
<dt><b>IDI_APPLICATION</b></dt>
<dt>MAKEINTRESOURCE(32512)</dt>
</dl>
</td>
<td width="60%">
Default application icon.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_ASTERISK"></a><a id="idi_asterisk"></a><dl>
<dt><b>IDI_ASTERISK</b></dt>
<dt>MAKEINTRESOURCE(32516)</dt>
</dl>
</td>
<td width="60%">
Asterisk icon. Same as <b>IDI_INFORMATION</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_ERROR"></a><a id="idi_error"></a><dl>
<dt><b>IDI_ERROR</b></dt>
<dt>MAKEINTRESOURCE(32513)</dt>
</dl>
</td>
<td width="60%">
Hand-shaped icon.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_EXCLAMATION"></a><a id="idi_exclamation"></a><dl>
<dt><b>IDI_EXCLAMATION</b></dt>
<dt>MAKEINTRESOURCE(32515)</dt>
</dl>
</td>
<td width="60%">
Exclamation point icon. Same as <b>IDI_WARNING</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_HAND"></a><a id="idi_hand"></a><dl>
<dt><b>IDI_HAND</b></dt>
<dt>MAKEINTRESOURCE(32513)</dt>
</dl>
</td>
<td width="60%">
Hand-shaped icon. Same as <b>IDI_ERROR</b>. 

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_INFORMATION"></a><a id="idi_information"></a><dl>
<dt><b>IDI_INFORMATION</b></dt>
<dt>MAKEINTRESOURCE(32516)</dt>
</dl>
</td>
<td width="60%">
Asterisk icon.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_QUESTION"></a><a id="idi_question"></a><dl>
<dt><b>IDI_QUESTION</b></dt>
<dt>MAKEINTRESOURCE(32514)</dt>
</dl>
</td>
<td width="60%">
Question mark icon.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_SHIELD"></a><a id="idi_shield"></a><dl>
<dt><b>IDI_SHIELD</b></dt>
<dt>MAKEINTRESOURCE(32518)</dt>
</dl>
</td>
<td width="60%">
Security Shield icon. 

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_WARNING"></a><a id="idi_warning"></a><dl>
<dt><b>IDI_WARNING</b></dt>
<dt>MAKEINTRESOURCE(32515)</dt>
</dl>
</td>
<td width="60%">
Exclamation point icon.

</td>
</tr>
<tr>
<td width="40%"><a id="IDI_WINLOGO"></a><a id="idi_winlogo"></a><dl>
<dt><b>IDI_WINLOGO</b></dt>
<dt>MAKEINTRESOURCE(32517)</dt>
</dl>
</td>
<td width="60%">
 
						Default application icon.

<b>Windows 2000:  </b>Windows logo icon.

</td>
</tr>
</table>

## -returns

Type: <b>HICON</b>

If the function succeeds, the return value is a handle to the newly loaded icon.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>LoadIcon</b> loads the icon resource only if it has not been loaded; otherwise, it retrieves a handle to the existing resource. The function searches the icon resource for the icon most appropriate for the current display. The icon resource can be a color or monochrome bitmap. 

<b>LoadIcon</b> can only load an icon whose size conforms to the <b>SM_CXICON</b> and <b>SM_CYICON</b> system metric values. Use the <a href="/windows/desktop/api/winuser/nf-winuser-loadimagea">LoadImage</a> function to load icons of other sizes.





> [!NOTE]
> The winuser.h header defines LoadIcon as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createicon">CreateIcon</a>



<a href="/windows/desktop/menurc/icons">Icons</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadimagea">LoadImage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>



<b>Reference</b>
