---
UID: NF:uxtheme.DrawThemeText
title: DrawThemeText function
author: windows-sdk-content
description: Draws text using the color and font defined by the visual style.
old-location: controls\DrawThemeText.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\drawthemetext.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: DrawThemeText, DrawThemeText function [Windows Controls], controls.DrawThemeText, controls.inet_DrawThemeText, inet_DrawThemeText, inet_DrawThemeText_cpp, uxtheme/DrawThemeText
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: BP_BUFFERFORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
api_name:
 - DrawThemeText
product: Windows
targetos: Windows
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# DrawThemeText function


## -description


Draws text using the color and font defined by the visual style.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's theme data. Use <a href="https://msdn.microsoft.com/library/Bb759821(v=VS.85).aspx">OpenThemeData</a> to create an HTHEME.


### -param hdc [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

HDC to use for drawing.


### -param iPartId [in]

Type: <b>int</b>

The control part that has the desired text appearance. See <a href="https://msdn.microsoft.com/library/Bb773210(v=VS.85).aspx">Parts and States</a>. If this value is 0, the text is drawn in the default font, or a font selected into the device context.


### -param iStateId [in]

Type: <b>int</b>

The control state that has the desired text appearance. See <a href="https://msdn.microsoft.com/library/Bb773210(v=VS.85).aspx">Parts and States</a>.


### -param pszText [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

Pointer to a string that contains the text to draw.


### -param cchText

TBD


### -param dwTextFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

<b>DWORD</b> that contains one or more values that specify the string's formatting. See <a href="https://msdn.microsoft.com/library/Bb773199(v=VS.85).aspx">Format Values</a> for possible parameter values. 

<div class="alert"><b>Note</b>  DrawThemeText does not support DT_CALCRECT.  However, <a href="https://msdn.microsoft.com/library/Bb773317(v=VS.85).aspx">DrawThemeTextEx</a> does support DT_CALCRECT.</div>
<div> </div>

### -param dwTextFlags2 [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Not used. Set to zero.


### -param pRect [in]

Type: <b>LPCRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the rectangle, in logical coordinates, in which the text is to be drawn.  It is recommended to use <b>pExtentRect</b> from <a href="https://msdn.microsoft.com/library/Bb759798(v=VS.85).aspx">GetThemeTextExtent</a> to retrieve the correct coordinates.


#### - iCharCount [in]

Type: <b>int</b>

Value of type <b>int</b> that contains the number of characters to draw. If the parameter is set to -1, all the characters in the string are drawn.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The function always uses the themed font for the specified part and state if one is defined. Otherwise it uses the font currently selected into the device context. To find out if a themed font is defined, you can call <a href="https://msdn.microsoft.com/library/Bb759745(v=VS.85).aspx">GetThemeFont</a> or <a href="https://msdn.microsoft.com/library/Bb759764(v=VS.85).aspx">GetThemePropertyOrigin</a> with TMT_FONT as the property identifier.


#### Examples

<b>DrawThemeText</b> uses parameters similar to the Win32 <a href="https://msdn.microsoft.com/fe412280-d797-4abd-8a29-107a9cd96145">DrawText</a> function, but with a few differences. One of the most notable is support for wide-character strings. Therefore, non-wide strings must be converted to wide strings, as in the following example. 

                    

<b>Security Warning:  </b>Using <a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a> incorrectly can compromise the security of your application. Ensure that when creating wide-character buffers they are large enough to accommodate the size of the string in wide characters, not in bytes.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>INT cchText = GetWindowTextLength(_hwnd);
if (cchText &gt; 0)
{
    TCHAR *pszText = new TCHAR[cchText+1];
    if (pszText)
    {
        if (GetWindowText(_hwnd, pszText, cchText+1))
        {
            int widelen = MultiByteToWideChar(CP_ACP, 0, reinterpret_cast&lt;LPCSTR&gt;(pszText), 
                    cchText+1, NULL, 0);
            WCHAR *pszWideText = new WCHAR[widelen+1];
            MultiByteToWideChar(CP_ACP, 0, reinterpret_cast&lt;LPCSTR&gt;(pszText), cchText, 
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
                    &amp;rcContent);

            delete [] pszWideText;
        }

        delete [] pszText;
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/Bb773213(v=VS.85).aspx">Property Identifiers</a>
 

 

