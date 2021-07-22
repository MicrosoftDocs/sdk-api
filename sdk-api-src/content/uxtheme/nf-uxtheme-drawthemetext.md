---
UID: NF:uxtheme.DrawThemeText
title: DrawThemeText function (uxtheme.h)
description: Draws text using the color and font defined by the visual style.
helpviewer_keywords: ["DrawThemeText","DrawThemeText function [Windows Controls]","controls.DrawThemeText","controls.inet_DrawThemeText","inet_DrawThemeText","inet_DrawThemeText_cpp","uxtheme/DrawThemeText"]
old-location: controls\DrawThemeText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\drawthemetext.htm
ms.date: 12/05/2018
ms.keywords: DrawThemeText, DrawThemeText function [Windows Controls], controls.DrawThemeText, controls.inet_DrawThemeText, inet_DrawThemeText, inet_DrawThemeText_cpp, uxtheme/DrawThemeText
req.header: uxtheme.h
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
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrawThemeText
 - uxtheme/DrawThemeText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
api_name:
 - DrawThemeText
---

# DrawThemeText function


## -description

Draws text using the color and font defined by the visual style.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's theme data. Use <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.

### -param hdc [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

HDC to use for drawing.

### -param iPartId [in]

Type: <b>int</b>

The control part that has the desired text appearance. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>. If this value is 0, the text is drawn in the default font, or a font selected into the device context.

### -param iStateId [in]

Type: <b>int</b>

The control state that has the desired text appearance. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param pszText [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

Pointer to a string that contains the text to draw.

### -param cchText [in]

Type: <b>int</b>

Value of type <b>int</b> that contains the number of characters to draw. If the parameter is set to -1, all the characters in the string are drawn.

### -param dwTextFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

<b>DWORD</b> that contains one or more values that specify the string's formatting. See <a href="/windows/desktop/Controls/theme-format-values">Format Values</a> for possible parameter values. 

<div class="alert"><b>Note</b>  DrawThemeText does not support DT_CALCRECT.  However, <a href="/windows/desktop/api/uxtheme/nf-uxtheme-drawthemetextex">DrawThemeTextEx</a> does support DT_CALCRECT.</div>
<div> </div>

### -param dwTextFlags2 [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Not used. Set to zero.

### -param pRect [in]

Type: <b>LPCRECT</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the rectangle, in logical coordinates, in which the text is to be drawn.  It is recommended to use <b>pExtentRect</b> from <a href="/windows/desktop/api/uxtheme/nf-uxtheme-getthemetextextent">GetThemeTextExtent</a> to retrieve the correct coordinates.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The function always uses the themed font for the specified part and state if one is defined. Otherwise it uses the font currently selected into the device context. To find out if a themed font is defined, you can call <a href="/windows/desktop/api/uxtheme/nf-uxtheme-getthemefont">GetThemeFont</a> or <a href="/windows/desktop/api/uxtheme/nf-uxtheme-getthemepropertyorigin">GetThemePropertyOrigin</a> with TMT_FONT as the property identifier.


#### Examples

<b>DrawThemeText</b> uses parameters similar to the Win32 <a href="/windows/desktop/api/winuser/nf-winuser-drawtext">DrawText</a> function, but with a few differences. One of the most notable is support for wide-character strings. Therefore, non-wide strings must be converted to wide strings, as in the following example. 

                    

<b>Security Warning:  </b>Using <a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a> incorrectly can compromise the security of your application. Ensure that when creating wide-character buffers they are large enough to accommodate the size of the string in wide characters, not in bytes.


```cpp
INT cchText = GetWindowTextLength(_hwnd);
if (cchText > 0)
{
    TCHAR *pszText = new TCHAR[cchText+1];
    if (pszText)
    {
        if (GetWindowText(_hwnd, pszText, cchText+1))
        {
            int widelen = MultiByteToWideChar(CP_ACP, 0, reinterpret_cast<LPCSTR>(pszText), 
                    cchText+1, NULL, 0);
            WCHAR *pszWideText = new WCHAR[widelen+1];
            MultiByteToWideChar(CP_ACP, 0, reinterpret_cast<LPCSTR>(pszText), cchText, 
                    pszWideText, widelen);

            SetBkMode(hdcPaint, TRANSPARENT);
            DrawThemeText(_hTheme,
                    hdcPaint,
                    BP_PUSHBUTTON,
                    _iStateId,
                    pszWideText,
                    cchText,
                    DT_CENTER | DT_VCENTER | DT_SINGLELINE,
                    NULL,
                    &rcContent);

            delete [] pszWideText;
        }

        delete [] pszText;
    }
}

```

## -see-also

<a href="/windows/desktop/Controls/property-typedefs">Property Identifiers</a>