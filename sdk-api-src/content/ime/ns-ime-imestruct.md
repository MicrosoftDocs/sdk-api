---
UID: NS:ime.tagIMESTRUCT
title: IMESTRUCT (ime.h)
description: Used by SendIMEMessageEx to specify the subfunction to be executed in the Input Method Editor (IME) message and its parameters. This structure is also used to receive return values from those subfunctions.
helpviewer_keywords: ["*LPIMESTRUCT","*NPIMESTRUCT","*PIMESTRUCT","IMESTRUCT","IMESTRUCT structure [Windows API]","IME_ENTERWORDREGISTERMODE","IME_GETCONVERSIONMODE","IME_GET_MODE","IME_MOVECONVERTWINDOW","IME_SETCONVERSIONFONTEX","IME_SETCONVERSIONMODE","IME_SETCONVERSIONWINDOW","IME_SETLEVEL","IME_SETOPEN","IME_SET_MODEK","PIMESTRUCT","PIMESTRUCT structure pointer [Windows API]","_win32_IMESTRUCT","ime/IMESTRUCT","ime/PIMESTRUCT","tagIMESTRUCT","winprog._win32_imestruct","winui._win32_imestruct"]
old-location: winprog\_win32_imestruct.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\imestruct.htm
ms.date: 12/05/2018
ms.keywords: '*LPIMESTRUCT, *NPIMESTRUCT, *PIMESTRUCT, IMESTRUCT, IMESTRUCT structure [Windows API], IME_ENTERWORDREGISTERMODE, IME_GETCONVERSIONMODE, IME_GET_MODE, IME_MOVECONVERTWINDOW, IME_SETCONVERSIONFONTEX, IME_SETCONVERSIONMODE, IME_SETCONVERSIONWINDOW, IME_SETLEVEL, IME_SETOPEN, IME_SET_MODEK, PIMESTRUCT, PIMESTRUCT structure pointer [Windows API], _win32_IMESTRUCT, ime/IMESTRUCT, ime/PIMESTRUCT, tagIMESTRUCT, winprog._win32_imestruct, winui._win32_imestruct'
req.header: ime.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: IMESTRUCT, *PIMESTRUCT, *NPIMESTRUCT, *LPIMESTRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagIMESTRUCT
 - ime/tagIMESTRUCT
 - PIMESTRUCT
 - ime/PIMESTRUCT
 - IMESTRUCT
 - ime/IMESTRUCT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ime.h
api_name:
 - IMESTRUCT
---

# IMESTRUCT structure


## -description

Used by <a href="/windows/desktop/api/ime/nf-ime-sendimemessageexa">SendIMEMessageEx</a> to specify the subfunction to be executed in the Input Method Editor (IME) message and its parameters. This structure is also used to receive return values from those subfunctions.

## -struct-fields

### -field fnc

A subfunction. One of the following values.



#### IME_ENTERWORDREGISTERMODE

Used to register words. Words are registered as an application sends a word and its reading. Structure members are interpreted as follows:

                        


<table class="clsStd">
<tr>
<th>Member</th>
<th>Type</th>
<th>Description</th>
</tr>
<tr>
<td><b>lParam1</b> [Windows 3.1]</td>
<td><b>LPARAM</b></td>
<td>The low-order word specifies a handle to the global memory that contains a word string ending with 0. The global memory is a memory block allocated by specifying the <b>GMEM_MOVEABLE</b> and <b>GMEM_SHARE</b> flags in the <a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> function.</td>
</tr>
<tr>
<td><b>lParam2</b> [Windows 3.1]</td>
<td><b>LPARAM</b></td>
<td>The low-order word specifies a handle to the global memory that contains a reading string ending with 0. The global memory is a memory block allocated by specifying the <b>GMEM_MOVEABLE</b> and <b>GMEM_SHARE</b> flags in the <a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> function</td>
</tr>
<tr>
<td><b>lParam3</b> [Windows 3.1]</td>
<td><b>LPARAM</b></td>
<td>Must be <b>NULL</b>.</td>
</tr>
<tr>
<td><b>lParam1</b> [Windows NT]</td>
<td><b>LPARAM</b></td>
<td>Specifies a handle to the global memory that contains a word string ending with 0. The global memory is a memory block allocated by specifying the <b>GMEM_MOVEABLE</b> and <b>GMEM_SHARE</b> flags in the <a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> function.</td>
</tr>
<tr>
<td><b>lParam2</b> [Windows NT]</td>
<td><b>LPARAM</b></td>
<td>Specifies a handle to the global memory that contains a reading string ending with 0. The global memory is a memory block allocated by specifying the <b>GMEM_MOVEABLE</b> and <b>GMEM_SHARE</b> flags in the <a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> function.</td>
</tr>
<tr>
<td><b>lParam3</b> [Windows NT]</td>
<td><b>LPARAM</b></td>
<td>Used to specify information about a part of speech. Since such information cannot be specified with the current Windows specification, <b>NULL</b> is set here.</td>
</tr>
</table>
 



The return value indicates the result of word registration. <b>TRUE</b> if the registration has been processed normally; otherwise, <b>FALSE</b>.

If information such as a part of speech is necessary, a dialog box should be displayed to prompt the user for input. <b>NULL</b> may be specified in the members <b>lParam1</b> and <b>lParam2</b>; in this case, nothing should be displayed in the associated entry field in the dialog box.



#### IME_GETCONVERSIONMODE

Acquires the current conversion mode of the IME. This subprogram uses no parameters.

                        

This is the same as <b>IME_GET_MODE</b>.

Returns the current conversion mode of the IME as a combination of <b>IME_MODE_ALPHANUMERIC</b> to <b>IME_MODE_NOCODEINPUT</b>. Conversion modes are as follows:


<table class="clsStd">
<tr>
<th>Conversion Mode</th>
<th>Mode</th>
</tr>
<tr>
<td><b>IME_MODE_ALPHANUMERIC</b></td>
<td>Alphanumeric</td>
</tr>
<tr>
<td><b>IME_MODE_KATAKANA</b></td>
<td>Katakana</td>
</tr>
<tr>
<td><b>IME_MODE_HIRAGANA</b></td>
<td>Hiragana</td>
</tr>
<tr>
<td><b>IME_MODE_SBCSCHAR</b></td>
<td>Single-byte character</td>
</tr>
<tr>
<td><b>IME_MODE_DBCSCHAR</b></td>
<td>Double-byte character</td>
</tr>
<tr>
<td><b>IME_MODE_ROMAN</b></td>
<td>Roman character</td>
</tr>
<tr>
<td><b>IME_MODE_NOROMAN</b></td>
<td>Non-Roman character</td>
</tr>
<tr>
<td><b>IME_MODE_CODEINPUT</b></td>
<td>Code input</td>
</tr>
<tr>
<td><b>IME_MODE_NOCODEINPUT</b></td>
<td>Non-code input</td>
</tr>
</table>
 





#### IME_GET_MODE

Same as <b>IME_GETCONVERSIONMODE</b>.



#### IME_MOVECONVERTWINDOW

Same as <b>IME_SETCONVERSIONWINDOW</b>.



#### IME_SETCONVERSIONFONTEX

A font to be used to display an undetermined string that appears in the conversion window. Structure members are interpreted as follows:

                        


<table class="clsStd">
<tr>
<th>Member</th>
<th>Type</th>
<th>Description</th>
</tr>
<tr>
<td><b>lParam1</b> [Windows 3.1]</td>
<td><b>LPARAM</b></td>
<td>The low-order word specifies a handle to the global memory that contains a <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure that specifies the logical font. The global memory is a memory block allocated by specifying the <b>GMEM_MOVEABLE</b> and <b>GMEM_SHARE</b> flags in the <a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> function. <b>NULL</b> indicates a system font.</td>
</tr>
<tr>
<td><b>lParam1</b> [Windows NT]</td>
<td><b>LPARAM</b></td>
<td>Specifies a handle to the global memory that contains a <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure that specifies the logical font. The global memory is a memory block allocated by specifying the <b>GMEM_MOVEABLE</b> and <b>GMEM_SHARE</b> flags in the <a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> function. <b>NULL</b> indicates a system font.</td>
</tr>
</table>
 



This subfunction has no return value.

The font specified by <b>IME_SETCONVERSIONFONTEX</b> can only be used to display undetermined strings.

To display undetermined strings at the default position, use a system font. If the display position is no longer the default position, enable the previously specified font.

The global memory that contains the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure is released by the application.

If the IME currently displaying the conversion window receives the <b>IME_SETCONVERSIONFONTEX</b> command, and as a result of the command processing the conversion window has changed, the IME should send a WM_IME_REPORT:IR_CHANGECONVERT message. This message should not be sent if the font specified by <b>IME_SETCONVERSIONFONTEX</b> is the same as the one being used by the IME.



#### IME_SETCONVERSIONMODE

Sets the conversion mode of the IME. The <b>wParam</b> member specifies one or more of the following values:

                        


<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>IME_MODE_ALPHANUMERIC</td>
<td>Alphanumeric conversion mode. This value cannot be used with IME_MODE_KATAKANA or IME_MODE_HIRAGANA.</td>
</tr>
<tr>
<td>IME_MODE_KATAKANA</td>
<td>Katakana conversion mode. This value cannot be used with IME_MODE_ALPHANUMERIC or IME_MODE_HIRAGANA.</td>
</tr>
<tr>
<td>IME_MODE_HIRAGANA</td>
<td>Hiragana conversion mode. This value cannot be used with IME_MODE_ALPHANUMERIC or IME_MODE_HIRAGANA.</td>
</tr>
<tr>
<td>IME_MODE_SBCSCHAR</td>
<td>Single-byte character conversion mode. This parameter cannot be used with IME_MODE_DBCSCHAR.</td>
</tr>
<tr>
<td>IME_MODE_DBCSCHAR</td>
<td>Double-byte character conversion mode. This parameter cannot be used with IME_MODE_SBCSCHAR.</td>
</tr>
<tr>
<td>IME_MODE_ROMAN</td>
<td>Roman character conversion mode. This parameter cannot be used with IME_MODE_NOROMAN.</td>
</tr>
<tr>
<td>IME_MODE_NOROMAN</td>
<td>Non-Roman character conversion mode. This parameter cannot be used with IME_MODE_ROMAN.</td>
</tr>
<tr>
<td>IME_MODE_CODEINPUT</td>
<td>Code input conversion mode. This parameter cannot be used with IME_MODE_NOCODEINPUT. How an IME operates in code input mode depends on the particular IME.</td>
</tr>
<tr>
<td>IME_MODE_NOCODEINPUT</td>
<td>Noncode input conversion mode. This parameter cannot be used with IME_MODE_CODEINPUT.</td>
</tr>
</table>
 



The return value indicates whether the given conversion mode has been set up successfully. It returns the state of the conversion mode previously in effect if the new conversion mode has been set up; otherwise, <b>NULL</b>.



#### IME_SETCONVERSIONWINDOW

The size and position of the bounding rectangle for the IME, and the initial position of the conversion window. The IME displays an undetermined string at the position specified by this subfunction. 

                        

The <b>wParam</b> member specifies one of the following values:

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>MCW_DEFAULT</td>
<td>Displays the conversion window at the default position, which is usually the bottom of the screen.

If the MCW_DEFAULT style is specified in an IME_SETCONVERSIONWINDOW message, then when the IME displays or draws a conversion window at the default position, it must not send an IR_OPENCONVERT, IR_CHANGECONVERT, IR_FULLCONVERT or IR_CLOSECONVERT message.

</td>
</tr>
<tr>
<td>MCW_WINDOW</td>
<td>Displays the conversion window at the coordinate given in the <b>lParam1</b> member, in the window specified in the <i>wParam</i> parameter of the WM_CONVERTREQUEST or WM_CONVERTREQUESTEX message. The value in <b>lParam1</b> indicates the coordinates relative to the upper left corner of the window, with the low-order word representing the X coordinate and the high-order word the Y coordinate. The bounding rectangle is the client rectangle of the given window and is the most typical way of invoking a kana-to-kanji conversion.

If the MCW_WINDOW style is specified in an IME_SETCONVERSIONWINDOW message, the IME must send an IR_OPENCOVERT message if the conversion window status has changed from closed to open. If the conversion window status has changed from open to closed, the IME must send an IR_CLOSECONVERT message. There is an exception, however. See IME_WINDOWUPDATE for details.

</td>
</tr>
<tr>
<td>MCW_WINDOW | MCW_RECT</td>
<td>Same as MCW_WINDOW except that the bounding rectangle is specified by the <b>lParam2</b> and <b>lParam3</b> members. The <b>lParam2</b> member specifies the upper-left point and <b>lParam3</b> specifies the lower-right point, each with the low-order word representing the X coordinate and the high-order word the Y coordinate. The coordinates are relative to the upper left of the window.</td>
</tr>
<tr>
<td>MCW_SCREEN</td>
<td>Displays the conversion window with its upper left corner designated by the <b>lParam1</b> member. The <b>lParam1</b> member indicates absolute coordinates with the origin at the upper left corner of the screen. The low-order word represents the X coordinate and the high-order word the Y coordinate. The bounding rectangle is the full screen.

If the MCW_SCREEN style is specified in an IME_SETCONVERSIONWINDOW message, the IME must send an IR_OPENCOVERT message if the conversion window status has changed from closed to open. If the conversion window status has changed from open to closed, the IME must send an IR_CLOSECONVERT message. There is an exception, however. See IME_WINDOWUPDATE for details.

</td>
</tr>
<tr>
<td>MCW_SCREEN | MCW_RECT</td>
<td>Same as MCW_SCREEN except that the bounding rectangle is specified by the <b>lParam2</b> and <b>lParam3</b> members. The <b>lParam2</b> member specifies the upper-left point and <b>lParam3</b> specifies the lower-right point, each with the low-order word representing the X coordinate and the high-order word the Y coordinate. The coordinates are absolute coordinates with the origin at the upper left of the screen.</td>
</tr>
<tr>
<td>MCW_HIDDEN [Windows 3.1]</td>
<td>When this flag is specified, the IME does not display the conversion window. Instead, the application itself displays undetermined strings. The <b>lParam1</b> member specifies the coordinates of the cursor position being displayed by the application or of the point of interest. The <b>lParam2</b> and <b>lParam3</b> members specify a region where no display is enabled by the IME. An IME that displays determined-string candidates in a pop-up window is able to use these pieces of information to determine where to display the window of determined-string candidates. A window to display candidate strings is considered as a system window. Therefore it is IME-dependent regarding whether to display such a window, where and how to display the window, and what keyboard input to use. The three members <b>lParam1</b>, <b>lParam2</b>, and <b>lParam3</b>, specify the absolute coordinates from the upper left of the screen, each with the low-order word representing the X coordinate and the high-order word the Y coordinate.

When the MCW_HIDDEN flag is specified, the IME sends an IR_UNDETERMINE message to request that the application displays the undetermined string. The application itself displays the undetermined string contained in this message.

Once the MCW_HIDDEN flag is specified, the IME does not send an IR_OPENCONVERT, IR_CHANGECONVERT or IR_CLOSECONVERT message.

If an application specifies MCW_HIDDEN and, at the same time, requests a rectangle too large to display the candidate window for a determined string, it should be treated as an error.  The error code must be IME_RD_TOOLONG.

If the MCW_HIDDEN style is specified in an IME_SETCONVERSIONWINDOW message, the IME must never send an IR_OPENCONVERT, IR_CHANGECONVERT, IR_FULLCONVERT or IR_CLOSECONVERT.

</td>
</tr>
<tr>
<td>MCW_VERTICAL</td>
<td>Tells the IME that the application is displaying character strings in vertical writing format. If this flag is specified, the conversion window is displayed for vertical writing, with the position designated by the <b>lParam1</b> member being the upper-right corner. This flag is can be specified with MCW_WINDOW, MCW_WINDOW|MCW_RECT, MCW_SCREEN, or MCW_SCREEN|MCW_RECT. An IME must support MCW_VERTICAL.
                                    
                                    If MCW_VERTICAL is specified and the font being selected is not for vertical writing, the IME uses the default vertical-writing font. This default font is created as follows:


<ol>
<li>Font information is retrieved in the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure by the <a href="/windows/desktop/api/wingdi/nf-wingdi-getobject">GetObject</a> function using the font handle of SYSTEM_FONT.</li>
<li>The font is created by adding an ampersand (@) at the beginning of the face name and setting the escapement and orientation to 270 degrees.</li>
</ol>


</td>
</tr>
</table>
 

The return value indicates whether the command has been executed. <b>TRUE</b> if the command execution was successful; otherwise, <b>FALSE</b>.

If an undetermined string seems to overflow the bounding rectangle, the IME must issue the report message WM_IME_REPORT:IR_FULLCONVERT to the application before displaying that string. If the application does not handle this message, the subsequent processing for the display is not formulated in this specification, but it is left to the IME. For example, the undetermined string might be scrolled within the bounding rectangle or it may be moved temporarily to the default position.

If an IME_SETCONVERSIONWINDOW message is called when the IME is holding an undetermined string, the IME should issue a WM_IME_REPORT:IR_CLOSECONVERT message; if the string fits in the window given as a parameter, the IME should issue a WM_IME_REPORT:IR_OPENCONVERT message. Only then should the conversion window be drawn. If the string does not fit in the window, the IME should issue a WM_IME_REPORT:IR_FULLCONVERT message.

The position of the bounding rectangle may be specified outside the physical screen area. If the whole bounding rectangle is outside the physical screen, undetermined strings must not be displayed.  If part of the bounding rectangle is outside the physical screen, the IME clips the bounding rectangle so that no part of the undetermined string overflows the screen, and also adjusts the display start position.

It is recommended not to set the maximum number of lines of, or maximum characters displayed in, the conversion window.

If the conversion window overlaps a system window, the conversion window must be visible. For example, the conversion window can be given top priority for display or the system window can be moved elsewhere.

The IME must send an IR_CHANGECONVERT message if the conversion window has changed in size, display contents, or display color. However, if an undetermined string does not fit in a specified window, the IME must send an IR_FULLCONVERT message rather than IR_CHANGECONVERT.

When the IME has shifted from the MCW_WINDOW or MCW_SCREEN mode to MCW_DEFAULT, it must send an IR_CLOSECONVERT message if an undetermined string exists.

When the IME has shifted from the MCW_WINDOW or MCW_SCREEN mode to MCW_HIDDEN, it must send an IR_CLOSECONVERT message if an undetermined string exists.

When the IME has shifted from the MCW_HIDDEN mode to MCW_DEFAULT, MCW_SCREEN, or MCW_WINDOW, the IME must transmit an IR_UNDETERMINE message with undetermined string = 0 and determined string = 0.



#### IME_SETLEVEL

Korean-specific subfunction that sets the IME level on the current application. The <b>wParam</b> member accepts one of the following level values.

<table class="clsStd">
<tr>
<th>Level</th>
<th>Meaning</th>
</tr>
<tr>
<td>1</td>
<td>No IME support. All IME-specific messages are ignored.</td>
</tr>
<tr>
<td>2</td>
<td>Partial IME support. Supports a subset of IME behavior including the position of the composition or candidate windows and the input mode or status.</td>
</tr>
<tr>
<td>3</td>
<td>Full IME support.</td>
</tr>
</table>
 



#### IME_SETOPEN

Sets the status of the kana-to-kanji conversion feature of the IME.

The <b>wParam</b> member is set to nonzero to open the IME and zero to close the IME

The return value indicates the previous status of the kana-to-kanji conversion feature. Returns <b>TRUE</b> if open; otherwise, <b>FALSE</b>.

An undetermined string must not be determined if the kana-to-kanji conversion feature has been closed by IME_SETOPEN.

When the kana-to-kanji conversion feature is to be closed by IME_SETOPEN, the IME must send an IR_CLOSECONVERT message if the IME is in MCW_WINDOW or MCW-SCREEN mode and if a conversion window is open. However, the IME need not issue IR_CLOSECONVERT if it is in MCW_HIDDEN mode and if an undetermined string exists.



#### IME_SET_MODEK

Korean-specific version of IME_SETCONVERSIONMODE.

### -field wParam

Usage depends on the subfunction specified in <b>fnc</b>.

### -field wCount

Usage depends on the subfunction specified in <b>fnc</b>.

### -field dchSource

Usage depends on the subfunction specified in <b>fnc</b>.

### -field dchDest

Usage depends on the subfunction specified in <b>fnc</b>.

### -field lParam1

Usage depends on the subfunction specified in <b>fnc</b>.

### -field lParam2

Usage depends on the subfunction specified in <b>fnc</b>.

### -field lParam3

Usage depends on the subfunction specified in <b>fnc</b>.

## -see-also

<a href="/windows/desktop/dataxchg/clipboard">Clipboard</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setclipboarddata">SetClipboardData</a>