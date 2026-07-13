---
UID: NF:winuser.GetMenuStringW
title: GetMenuStringW function (winuser.h)
description: Copies the text string of the specified menu item into the specified buffer. (Unicode)
helpviewer_keywords: ["GetMenuString", "GetMenuString function [Menus and Other Resources]", "GetMenuStringW", "MF_BYCOMMAND", "MF_BYPOSITION", "_win32_GetMenuString", "_win32_getmenustring_cpp", "menurc.getmenustring", "winui._win32_getmenustring", "winuser/GetMenuString", "winuser/GetMenuStringW"]
old-location: menurc\getmenustring.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\getmenustring.htm
ms.date: 12/05/2018
ms.keywords: GetMenuString, GetMenuString function [Menus and Other Resources], GetMenuStringA, GetMenuStringW, MF_BYCOMMAND, MF_BYPOSITION, _win32_GetMenuString, _win32_getmenustring_cpp, menurc.getmenustring, winui._win32_getmenustring, winuser/GetMenuString, winuser/GetMenuStringA, winuser/GetMenuStringW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetMenuStringW (Unicode) and GetMenuStringA (ANSI)
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
 - GetMenuStringW
 - winuser/GetMenuStringW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Menu-l1-1-0.dll
 - Ext-MS-Win-NTUser-Menu-l1-1-1.dll
 - ext-ms-win-ntuser-menu-l1-1-2.dll
 - Ext-MS-Win-NTUser-Menu-L1-1-3.dll
api_name:
 - GetMenuString
 - GetMenuStringA
 - GetMenuStringW
req.apiset: ext-ms-win-ntuser-menu-l1-1-3 (introduced in Windows 10, version 10.0.14393)
---

# GetMenuStringW function


## -description

Copies the text string of the specified menu item into the specified buffer. 
<div class="alert"><b>Note</b>  The <b>GetMenuString</b> function has been superseded. Use the <a href="/windows/desktop/api/winuser/nf-winuser-getmenuiteminfoa">GetMenuItemInfo</a> function to retrieve the menu item text.</div><div> </div>

## -parameters

### -param hMenu [in]

Type: <b>HMENU</b>

A handle to the menu.

### -param uIDItem [in]

Type: <b>UINT</b>

The menu item to be changed, as determined by the <i>uFlag</i> parameter.

### -param lpString [out, optional]

Type: <b>LPTSTR</b>

The buffer that receives the null-terminated string. If the string is as long or longer than <i>lpString</i>, the string is truncated and the terminating null character is added. If <i>lpString</i> is <b>NULL</b>, the function returns the length of the menu string.

### -param cchMax [in]

Type: <b>int</b>

The maximum length, in characters, of the string to be copied. If the string is longer than the maximum specified in the <i>nMaxCount</i> parameter, the extra characters are truncated. If <i>nMaxCount</i> is 0, the function returns the length of the menu string.

### -param flags [in]

Type: <b>UINT</b>

Indicates how the <i>uIDItem</i> parameter is interpreted. This parameter must be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MF_BYCOMMAND"></a><a id="mf_bycommand"></a><dl>
<dt><b>MF_BYCOMMAND</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Indicates that <i>uIDItem</i> gives the identifier of the menu item. If neither the <b>MF_BYCOMMAND</b> nor <b>MF_BYPOSITION</b> flag is specified, the <b>MF_BYCOMMAND</b> flag is the default flag.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_BYPOSITION"></a><a id="mf_byposition"></a><dl>
<dt><b>MF_BYPOSITION</b></dt>
<dt>0x00000400L</dt>
</dl>
</td>
<td width="60%">
Indicates that <i>uIDItem</i> gives the zero-based relative position of the menu item.

</td>
</tr>
</table>

## -returns

Type: <b>int</b>

If the function succeeds, the return value specifies the number of characters copied to the buffer, not including the terminating null character.

If the function fails, the return value is zero. 

If the specified item is not of type <b>MIIM_STRING</b> or <b>MFT_STRING</b>, then the return value is zero.

## -remarks

The <i>nMaxCount</i> parameter must be one larger than the number of characters in the text string to accommodate the terminating null character. 

If <i>nMaxCount</i> is 0, the function returns the length of the menu string.

<h3><a id="Security_Warning"></a><a id="security_warning"></a><a id="SECURITY_WARNING"></a>Security Warning</h3>
The <i>lpString</i> parameter is a <b>TCHAR</b> buffer, and <i>nMaxCount</i> is the length of the menu string in characters. Sizing these parameters incorrectly can cause truncation of the string, leading to possible loss of data.


#### Examples

For an example, see <a href="/windows/desktop/menurc/using-keyboard-accelerators">Creating User Editable Accelerators</a>. 

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines GetMenuString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getmenuitemid">GetMenuItemID</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>
