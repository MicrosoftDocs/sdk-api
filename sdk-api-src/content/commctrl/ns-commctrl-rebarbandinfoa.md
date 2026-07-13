---
UID: NS:commctrl.tagREBARBANDINFOA
title: REBARBANDINFOA (commctrl.h)
description: Contains information that defines a band in a rebar control. (ANSI)
helpviewer_keywords: ["*LPREBARBANDINFOA","LPREBARBANDINFO","LPREBARBANDINFO structure pointer [Windows Controls]","RBBIM_BACKGROUND","RBBIM_CHEVRONLOCATION","RBBIM_CHEVRONSTATE","RBBIM_CHILD","RBBIM_CHILDSIZE","RBBIM_COLORS","RBBIM_HEADERSIZE","RBBIM_ID","RBBIM_IDEALSIZE","RBBIM_IMAGE","RBBIM_LPARAM","RBBIM_SIZE","RBBIM_STYLE","RBBIM_TEXT","RBBS_BREAK","RBBS_CHILDEDGE","RBBS_FIXEDBMP","RBBS_FIXEDSIZE","RBBS_GRIPPERALWAYS","RBBS_HIDDEN","RBBS_HIDETITLE","RBBS_NOGRIPPER","RBBS_NOVERT","RBBS_TOPALIGN","RBBS_USECHEVRON","RBBS_VARIABLEHEIGHT","REBARBANDINFO","REBARBANDINFO structure [Windows Controls]","REBARBANDINFOA","REBARBANDINFOW","_win32_REBARBANDINFO","_win32_REBARBANDINFO_cpp","commctrl/LPREBARBANDINFO","commctrl/REBARBANDINFO","commctrl/REBARBANDINFOA","commctrl/REBARBANDINFOW","controls.REBARBANDINFO","controls._win32_REBARBANDINFO"]
old-location: controls\REBARBANDINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\rebar\structures\rebarbandinfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPREBARBANDINFOA, LPREBARBANDINFO, LPREBARBANDINFO structure pointer [Windows Controls], RBBIM_BACKGROUND, RBBIM_CHEVRONLOCATION, RBBIM_CHEVRONSTATE, RBBIM_CHILD, RBBIM_CHILDSIZE, RBBIM_COLORS, RBBIM_HEADERSIZE, RBBIM_ID, RBBIM_IDEALSIZE, RBBIM_IMAGE, RBBIM_LPARAM, RBBIM_SIZE, RBBIM_STYLE, RBBIM_TEXT, RBBS_BREAK, RBBS_CHILDEDGE, RBBS_FIXEDBMP, RBBS_FIXEDSIZE, RBBS_GRIPPERALWAYS, RBBS_HIDDEN, RBBS_HIDETITLE, RBBS_NOGRIPPER, RBBS_NOVERT, RBBS_TOPALIGN, RBBS_USECHEVRON, RBBS_VARIABLEHEIGHT, REBARBANDINFO, REBARBANDINFO structure [Windows Controls], REBARBANDINFOA, REBARBANDINFOW, _win32_REBARBANDINFO, _win32_REBARBANDINFO_cpp, commctrl/LPREBARBANDINFO, commctrl/REBARBANDINFO, commctrl/REBARBANDINFOA, commctrl/REBARBANDINFOW, controls.REBARBANDINFO, controls._win32_REBARBANDINFO'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: REBARBANDINFOW (Unicode) and REBARBANDINFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: REBARBANDINFOA, *LPREBARBANDINFOA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagREBARBANDINFOA
 - commctrl/tagREBARBANDINFOA
 - LPREBARBANDINFOA
 - commctrl/LPREBARBANDINFOA
 - REBARBANDINFOA
 - commctrl/REBARBANDINFOA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - REBARBANDINFO
 - REBARBANDINFOA
 - REBARBANDINFOW
---

# REBARBANDINFOA structure


## -description

Contains information that defines a band in a rebar control.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of this structure, in bytes. Your application must fill this member before sending any messages that use the address of this structure as a parameter.

### -field fMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags that indicate which members of this structure are valid or must be filled. This value can be a combination of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RBBIM_BACKGROUND"></a><a id="rbbim_background"></a><dl>
<dt><b>RBBIM_BACKGROUND</b></dt>
</dl>
</td>
<td width="60%">
The <b>hbmBack</b> member is valid or must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBIM_CHILD"></a><a id="rbbim_child"></a><dl>
<dt><b>RBBIM_CHILD</b></dt>
</dl>
</td>
<td width="60%">
The <b>hwndChild</b> member is valid or must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBIM_CHILDSIZE"></a><a id="rbbim_childsize"></a><dl>
<dt><b>RBBIM_CHILDSIZE</b></dt>
</dl>
</td>
<td width="60%">
The <b>cxMinChild</b>, <b>cyMinChild</b>, <b>cyChild</b>, <b>cyMaxChild</b>, and <b>cyIntegral</b> members are valid or must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBIM_COLORS"></a><a id="rbbim_colors"></a><dl>
<dt><b>RBBIM_COLORS</b></dt>
</dl>
</td>
<td width="60%">
The <b>clrFore</b> and <b>clrBack</b> members are valid or must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBIM_HEADERSIZE"></a><a id="rbbim_headersize"></a><dl>
<dt><b>RBBIM_HEADERSIZE</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 4.71</a>. The <b>cxHeader</b> member is valid or must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBIM_IDEALSIZE"></a><a id="rbbim_idealsize"></a><dl>
<dt><b>RBBIM_IDEALSIZE</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 4.71</a>. The <b>cxIdeal</b> member is valid or must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBIM_ID"></a><a id="rbbim_id"></a><dl>
<dt><b>RBBIM_ID</b></dt>
</dl>
</td>
<td width="60%">
The <b>wID</b> member is valid or must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBIM_IMAGE"></a><a id="rbbim_image"></a><dl>
<dt><b>RBBIM_IMAGE</b></dt>
</dl>
</td>
<td width="60%">
The <b>iImage</b> member is valid or must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBIM_LPARAM"></a><a id="rbbim_lparam"></a><dl>
<dt><b>RBBIM_LPARAM</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 4.71</a>. The <b>lParam</b> member is valid or must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBIM_SIZE"></a><a id="rbbim_size"></a><dl>
<dt><b>RBBIM_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <b>cx</b> member is valid or must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBIM_STYLE"></a><a id="rbbim_style"></a><dl>
<dt><b>RBBIM_STYLE</b></dt>
</dl>
</td>
<td width="60%">
The <b>fStyle</b> member is valid or must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBIM_TEXT"></a><a id="rbbim_text"></a><dl>
<dt><b>RBBIM_TEXT</b></dt>
</dl>
</td>
<td width="60%">
The <b>lpText</b> member is valid or must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBIM_CHEVRONLOCATION"></a><a id="rbbim_chevronlocation"></a><dl>
<dt><b>RBBIM_CHEVRONLOCATION</b></dt>
</dl>
</td>
<td width="60%">
The <b>rcChevronLocation</b> member is valid or must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBIM_CHEVRONSTATE"></a><a id="rbbim_chevronstate"></a><dl>
<dt><b>RBBIM_CHEVRONSTATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>uChevronState</b> member is valid or must be set.

</td>
</tr>
</table>

### -field fStyle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags that specify the band style. This value can be a combination of the following:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RBBS_BREAK"></a><a id="rbbs_break"></a><dl>
<dt><b>RBBS_BREAK</b></dt>
</dl>
</td>
<td width="60%">
The band is on a new line.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBS_CHILDEDGE"></a><a id="rbbs_childedge"></a><dl>
<dt><b>RBBS_CHILDEDGE</b></dt>
</dl>
</td>
<td width="60%">
The band has an edge at the top and bottom of the child window.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBS_FIXEDBMP"></a><a id="rbbs_fixedbmp"></a><dl>
<dt><b>RBBS_FIXEDBMP</b></dt>
</dl>
</td>
<td width="60%">
The background bitmap does not move when the band is resized.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBS_FIXEDSIZE"></a><a id="rbbs_fixedsize"></a><dl>
<dt><b>RBBS_FIXEDSIZE</b></dt>
</dl>
</td>
<td width="60%">
The band can't be sized. With this style, the sizing grip is not displayed on the band.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBS_GRIPPERALWAYS"></a><a id="rbbs_gripperalways"></a><dl>
<dt><b>RBBS_GRIPPERALWAYS</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 4.71</a>. The band will always have a sizing grip, even if it is the only band in the rebar.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBS_HIDDEN"></a><a id="rbbs_hidden"></a><dl>
<dt><b>RBBS_HIDDEN</b></dt>
</dl>
</td>
<td width="60%">
The band will not be visible.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBS_NOGRIPPER"></a><a id="rbbs_nogripper"></a><dl>
<dt><b>RBBS_NOGRIPPER</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 4.71</a>. The band will never have a sizing grip, even if there is more than one band in the rebar.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBS_USECHEVRON"></a><a id="rbbs_usechevron"></a><dl>
<dt><b>RBBS_USECHEVRON</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 5.80.</a> Show a chevron button if the band is smaller than <b>cxIdeal</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBS_VARIABLEHEIGHT"></a><a id="rbbs_variableheight"></a><dl>
<dt><b>RBBS_VARIABLEHEIGHT</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 4.71</a>. The band can be resized by the rebar control; <b>cyIntegral</b> and <b>cyMaxChild</b> affect how the rebar will resize the band.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBS_NOVERT"></a><a id="rbbs_novert"></a><dl>
<dt><b>RBBS_NOVERT</b></dt>
</dl>
</td>
<td width="60%">
Do not show when vertical.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBS_HIDETITLE"></a><a id="rbbs_hidetitle"></a><dl>
<dt><b>RBBS_HIDETITLE</b></dt>
</dl>
</td>
<td width="60%">
Keep band title hidden.

</td>
</tr>
<tr>
<td width="40%"><a id="RBBS_TOPALIGN"></a><a id="rbbs_topalign"></a><dl>
<dt><b>RBBS_TOPALIGN</b></dt>
</dl>
</td>
<td width="60%">
Keep band in top row.

</td>
</tr>
</table>

### -field clrFore

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

Band foreground colors.

### -field clrBack

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

Band background colors. If <b>hbmBack</b> specifies a background bitmap, these members are ignored. By default, the band will use the background color of the rebar control set with the <a href="/windows/desktop/Controls/rb-setbkcolor">RB_SETBKCOLOR</a> message. If a background color is specified here, then this background color will be used instead.

### -field lpText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

Pointer to a buffer that contains the display text for the band. If band information is being requested from the control and  RBBIM_TEXT is specified in <b>fMask</b>, this member must be initialized to the address of the buffer that will receive the text.

### -field cch

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the buffer at <b>lpText</b>, in bytes. If information is not being requested from the control, this member is ignored.

### -field iImage

Type: <b>int</b>

Zero-based index of any image that should be displayed in the band. The image list is set using the <a href="/windows/desktop/Controls/rb-setbarinfo">RB_SETBARINFO</a> message.

### -field hwndChild

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the child window contained in the band, if any.

### -field cxMinChild

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Minimum width of the child window, in pixels. The band can't be sized smaller than this value.

### -field cyMinChild

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Minimum height of the child window, in pixels. The band can't be sized smaller than this value.

### -field cx

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Length of the band, in pixels.

### -field hbmBack

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HBITMAP</a></b>

Handle to a bitmap that is used as the background for this band.

### -field wID

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

UINT value that the control uses to identify this band for custom draw notification messages.

### -field cyChild

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 4.71</a>. Initial height of the band, in pixels. This member is ignored unless the RBBS_VARIABLEHEIGHT style is specified.

### -field cyMaxChild

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 4.71</a>. Maximum height of the band, in pixels. This member is ignored unless the RBBS_VARIABLEHEIGHT style is specified.

### -field cyIntegral

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 4.71</a>. Step value by which the band can grow or shrink, in pixels. If the band is resized, it will be resized in steps specified by this value. This member is ignored unless the  RBBS_VARIABLEHEIGHT style is specified.

### -field cxIdeal

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 4.71</a>. Ideal width of the band, in pixels. If the band is maximized to the ideal width (see <a href="/windows/desktop/Controls/rb-maximizeband">RB_MAXIMIZEBAND</a>), the rebar control will attempt to make the band this width.

### -field lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 4.71</a>. Application-defined value.

### -field cxHeader

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 4.71</a>. Size of the band's header, in pixels. The band header is the area between the edge of the band and the edge of the child window. This is the area where band text and images are displayed, if they are specified. If this value is specified, it will override the normal header dimensions that the control calculates for the band.

### -field rcChevronLocation

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 6</a>. Location of the chevron.

### -field uChevronState

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 6</a>. A combination of the <a href="/windows/desktop/WinAuto/object-state-constants">Object State Constants</a>.

## -remarks

The <b>cxMinChild</b>, <b>cyMinChild</b>, and <b>cx</b> members provide information on dimensions relative to the orientation of the control. That is, for a horizontal rebar control, <b>cxMinChild</b> and <b>cx</b> are horizontal measurements and <b>cyMinChild</b> is a vertical measurement. However, if the control uses the <a href="/windows/desktop/Controls/common-control-styles">CCS_VERT</a> style, <b>cxMinChild</b> and <b>cx</b> are vertical measurements and <b>cyMinChild</b> is a horizontal measurement. 




> [!NOTE]
> The commctrl.h header defines REBARBANDINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
