---
UID: NS:richedit._charformat
title: "_charformat"
author: windows-sdk-content
description: Contains information about character formatting in a rich edit control.
old-location: controls\CHARFORMAT.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\charformat.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CFE_AUTOCOLOR, CFE_BOLD, CFE_DISABLED, CFE_ITALIC, CFE_PROTECTED, CFE_STRIKEOUT, CFE_UNDERLINE, CFM_ALL, CFM_BOLD, CFM_CHARSET, CFM_COLOR, CFM_EFFECTS, CFM_FACE, CFM_ITALIC, CFM_OFFSET, CFM_PROTECTED, CFM_SIZE, CFM_STRIKEOUT, CFM_UNDERLINE., CHARFORMAT, CHARFORMAT structure [Windows Controls], CHARFORMATA, CHARFORMATW, _charformat, _win32_CHARFORMAT_str, _win32_CHARFORMAT_str_cpp, controls.CHARFORMAT, controls._win32_CHARFORMAT_str, richedit/CHARFORMAT, richedit/CHARFORMATA, richedit/CHARFORMATW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CHARFORMATW (Unicode) and CHARFORMATA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - CHARFORMAT
 - CHARFORMATA
 - CHARFORMATW
product: Windows
targetos: Windows
req.typenames: CHARFORMATA
req.redist: 
---

# _charformat structure


## -description


Contains information about character formatting in a rich edit control.
        

<b>Rich Edit 2.0:</b> The <a href="https://msdn.microsoft.com/en-us/library/Bb787883(v=VS.85).aspx">CHARFORMAT2</a> structure is a Microsoft Rich Edit 2.0 extension of the <b>CHARFORMAT</b> structure. Microsoft Rich Edit 2.0 and later allows you to use either structure with the <a href="https://msdn.microsoft.com/en-us/library/Bb788026(v=VS.85).aspx">EM_GETCHARFORMAT</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb774230(v=VS.85).aspx">EM_SETCHARFORMAT</a> messages. 


## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size in bytes of the specified structure. This member must be set before passing the structure to the rich edit control. 


### -field dwMask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Members containing valid information or attributes to set. This member can be zero, one, or more than one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CFM_ALL"></a><a id="cfm_all"></a><dl>
<dt><b>CFM_ALL</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows 8</b>: A combination of the following values: CFM_EFFECTS | CFM_SIZE | CFM_FACE | CFM_OFFSET | CFM_CHARSET

</td>
</tr>
<tr>
<td width="40%"><a id="CFM_BOLD"></a><a id="cfm_bold"></a><dl>
<dt><b>CFM_BOLD</b></dt>
</dl>
</td>
<td width="60%">
The CFE_BOLD value of the <b>dwEffects</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="CFM_CHARSET"></a><a id="cfm_charset"></a><dl>
<dt><b>CFM_CHARSET</b></dt>
</dl>
</td>
<td width="60%">
The <b>bCharSet</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="CFM_COLOR"></a><a id="cfm_color"></a><dl>
<dt><b>CFM_COLOR</b></dt>
</dl>
</td>
<td width="60%">
The <b>crTextColor</b> member and the CFE_AUTOCOLOR value of the <b>dwEffects</b> member are valid.

</td>
</tr>
<tr>
<td width="40%"><a id="CFM_EFFECTS"></a><a id="cfm_effects"></a><dl>
<dt><b>CFM_EFFECTS</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows 8</b>: A combination of the following values: CFM_BOLD | CFM_ITALIC | CFM_UNDERLINE | CFM_COLOR | CFM_STRIKEOUT | CFE_PROTECTED | CFM_LINK

</td>
</tr>
<tr>
<td width="40%"><a id="CFM_FACE"></a><a id="cfm_face"></a><dl>
<dt><b>CFM_FACE</b></dt>
</dl>
</td>
<td width="60%">
The <b>szFaceName</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="CFM_ITALIC"></a><a id="cfm_italic"></a><dl>
<dt><b>CFM_ITALIC</b></dt>
</dl>
</td>
<td width="60%">
The CFE_ITALIC value of the <b>dwEffects</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="CFM_OFFSET"></a><a id="cfm_offset"></a><dl>
<dt><b>CFM_OFFSET</b></dt>
</dl>
</td>
<td width="60%">
The <b>yOffset</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="CFM_PROTECTED"></a><a id="cfm_protected"></a><dl>
<dt><b>CFM_PROTECTED</b></dt>
</dl>
</td>
<td width="60%">
The CFE_PROTECTED value of the <b>dwEffects</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="CFM_SIZE"></a><a id="cfm_size"></a><dl>
<dt><b>CFM_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <b>yHeight</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="CFM_STRIKEOUT"></a><a id="cfm_strikeout"></a><dl>
<dt><b>CFM_STRIKEOUT</b></dt>
</dl>
</td>
<td width="60%">
The CFE_STRIKEOUT value of the <b>dwEffects</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="CFM_UNDERLINE."></a><a id="cfm_underline."></a><dl>
<dt><b>CFM_UNDERLINE.</b></dt>
</dl>
</td>
<td width="60%">
The CFE_UNDERLINE value of the <b>dwEffects</b> member is valid.

</td>
</tr>
</table>
 


### -field dwEffects

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Character effects. This member can be a combination of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CFE_AUTOCOLOR"></a><a id="cfe_autocolor"></a><dl>
<dt><b>CFE_AUTOCOLOR</b></dt>
</dl>
</td>
<td width="60%">
The text color is the return value of <a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a>(COLOR_WINDOWTEXT).

</td>
</tr>
<tr>
<td width="40%"><a id="CFE_BOLD"></a><a id="cfe_bold"></a><dl>
<dt><b>CFE_BOLD</b></dt>
</dl>
</td>
<td width="60%">
Characters are bold.

</td>
</tr>
<tr>
<td width="40%"><a id="CFE_DISABLED"></a><a id="cfe_disabled"></a><dl>
<dt><b>CFE_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
<b>RichEdit 2.0 and later:</b> Characters are displayed with a shadow that is offset by 3/4 point or one pixel, whichever is larger.

</td>
</tr>
<tr>
<td width="40%"><a id="CFE_ITALIC"></a><a id="cfe_italic"></a><dl>
<dt><b>CFE_ITALIC</b></dt>
</dl>
</td>
<td width="60%">
Characters are italic.

</td>
</tr>
<tr>
<td width="40%"><a id="CFE_STRIKEOUT"></a><a id="cfe_strikeout"></a><dl>
<dt><b>CFE_STRIKEOUT</b></dt>
</dl>
</td>
<td width="60%">
Characters are struck.

</td>
</tr>
<tr>
<td width="40%"><a id="CFE_UNDERLINE"></a><a id="cfe_underline"></a><dl>
<dt><b>CFE_UNDERLINE</b></dt>
</dl>
</td>
<td width="60%">
Characters are underlined.

</td>
</tr>
<tr>
<td width="40%"><a id="CFE_PROTECTED"></a><a id="cfe_protected"></a><dl>
<dt><b>CFE_PROTECTED</b></dt>
</dl>
</td>
<td width="60%">
Characters are protected; an attempt to modify them will cause an <a href="https://msdn.microsoft.com/en-us/library/Bb787981(v=VS.85).aspx">EN_PROTECTED</a> notification code.

</td>
</tr>
</table>
 


### -field yHeight

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Character height, in twips (1/1440 of an inch or 1/20 of a printer's point). 


### -field yOffset

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Character offset, in twips, from the baseline. If the value of this member is positive, the character is a superscript; if it is negative, the character is a subscript. 


### -field crTextColor

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

Text color. This member is ignored if the CFE_AUTOCOLOR character effect is specified. To generate a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro. 


### -field bCharSet

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Character set value. The 
					<b>bCharSet</b> member can be one of the values specified for the 
					<b>lfCharSet</b> member of the <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> structure. Microsoft Rich Edit 3.0 may override this value if it is invalid for the target characters. 


### -field bPitchAndFamily

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Font family and pitch. This member is the same as the <b>lfPitchAndFamily</b> member of the <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> structure. 


### -field szFaceName

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">TCHAR</a>[LF_FACESIZE]</b>

Null-terminated character array specifying the font name. 


## -remarks



To turn off a formatting attribute, set the appropriate value in <b>dwMask</b> but do not set the corresponding value in <b>dwEffects</b>. For example, to turn off italics, set CFM_ITALIC but do not set CFE_ITALIC.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb787883(v=VS.85).aspx">CHARFORMAT2</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb788026(v=VS.85).aspx">EM_GETCHARFORMAT</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774230(v=VS.85).aspx">EM_SETCHARFORMAT</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787981(v=VS.85).aspx">EN_PROTECTED</a>



<b>Reference</b>
 

 

