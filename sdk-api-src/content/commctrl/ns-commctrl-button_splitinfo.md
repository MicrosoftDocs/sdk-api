---
UID: NS:commctrl.tagBUTTON_SPLITINFO
title: BUTTON_SPLITINFO (commctrl.h)
description: Contains information that defines a split button (BS_SPLITBUTTON and BS_DEFSPLITBUTTON styles). Used with the BCM_GETSPLITINFO and BCM_SETSPLITINFO messages.
helpviewer_keywords: ["*PBUTTON_SPLITINFO","BCSIF_GLYPH","BCSIF_IMAGE","BCSIF_SIZE","BCSIF_STYLE","BCSS_ALIGNLEFT","BCSS_IMAGE","BCSS_NOSPLIT","BCSS_STRETCH","BUTTON_SPLITINFO","BUTTON_SPLITINFO structure [Windows Controls]","PBUTTON_SPLITINFO","PBUTTON_SPLITINFO structure pointer [Windows Controls]","_shell_BUTTON_SPLITINFO_str","_shell_BUTTON_SPLITINFO_str_cpp","commctrl/BUTTON_SPLITINFO","commctrl/PBUTTON_SPLITINFO","controls.BUTTON_SPLITINFO","controls._shell_BUTTON_SPLITINFO_str"]
old-location: controls\BUTTON_SPLITINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonstructures\button_splitinfo.htm
ms.date: 12/05/2018
ms.keywords: '*PBUTTON_SPLITINFO, BCSIF_GLYPH, BCSIF_IMAGE, BCSIF_SIZE, BCSIF_STYLE, BCSS_ALIGNLEFT, BCSS_IMAGE, BCSS_NOSPLIT, BCSS_STRETCH, BUTTON_SPLITINFO, BUTTON_SPLITINFO structure [Windows Controls], PBUTTON_SPLITINFO, PBUTTON_SPLITINFO structure pointer [Windows Controls], _shell_BUTTON_SPLITINFO_str, _shell_BUTTON_SPLITINFO_str_cpp, commctrl/BUTTON_SPLITINFO, commctrl/PBUTTON_SPLITINFO, controls.BUTTON_SPLITINFO, controls._shell_BUTTON_SPLITINFO_str'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: BUTTON_SPLITINFO, *PBUTTON_SPLITINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagBUTTON_SPLITINFO
 - commctrl/tagBUTTON_SPLITINFO
 - PBUTTON_SPLITINFO
 - commctrl/PBUTTON_SPLITINFO
 - BUTTON_SPLITINFO
 - commctrl/BUTTON_SPLITINFO
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
 - BUTTON_SPLITINFO
---

# BUTTON_SPLITINFO structure


## -description

Contains information that defines a split button (<a href="/windows/desktop/Controls/button-styles">BS_SPLITBUTTON</a> and <a href="/windows/desktop/Controls/button-styles">BS_DEFSPLITBUTTON</a> styles). Used with the <a href="/windows/desktop/Controls/bcm-getsplitinfo">BCM_GETSPLITINFO</a> and <a href="/windows/desktop/Controls/bcm-setsplitinfo">BCM_SETSPLITINFO</a> messages.

## -struct-fields

### -field mask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A set of flags that specify which members of this structure contain data to be set or which members are being requested. Set this member to one or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCSIF_GLYPH"></a><a id="bcsif_glyph"></a><dl>
<dt><b>BCSIF_GLYPH</b></dt>
</dl>
</td>
<td width="60%">
<b>himlGlyph</b> is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="BCSIF_IMAGE"></a><a id="bcsif_image"></a><dl>
<dt><b>BCSIF_IMAGE</b></dt>
</dl>
</td>
<td width="60%">
<b>himlGlyph</b> is valid. Use when <b>uSplitStyle</b> is set to BCSS_IMAGE.

</td>
</tr>
<tr>
<td width="40%"><a id="BCSIF_SIZE"></a><a id="bcsif_size"></a><dl>
<dt><b>BCSIF_SIZE</b></dt>
</dl>
</td>
<td width="60%">
<b>size</b> is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="BCSIF_STYLE"></a><a id="bcsif_style"></a><dl>
<dt><b>BCSIF_STYLE</b></dt>
</dl>
</td>
<td width="60%">
<b>uSplitStyle</b> is valid.

</td>
</tr>
</table>

### -field himlGlyph

Type: <b>HIMAGELIST</b>

A handle to the image list. The provider retains ownership of the image list and is ultimately responsible for its disposal.

### -field uSplitStyle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The split button style. Value must be one or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCSS_ALIGNLEFT"></a><a id="bcss_alignleft"></a><dl>
<dt><b>BCSS_ALIGNLEFT</b></dt>
</dl>
</td>
<td width="60%">
Align the image or glyph horizontally with the left margin.

</td>
</tr>
<tr>
<td width="40%"><a id="BCSS_IMAGE"></a><a id="bcss_image"></a><dl>
<dt><b>BCSS_IMAGE</b></dt>
</dl>
</td>
<td width="60%">
Draw an icon image as the glyph.

</td>
</tr>
<tr>
<td width="40%"><a id="BCSS_NOSPLIT"></a><a id="bcss_nosplit"></a><dl>
<dt><b>BCSS_NOSPLIT</b></dt>
</dl>
</td>
<td width="60%">
No split.

</td>
</tr>
<tr>
<td width="40%"><a id="BCSS_STRETCH"></a><a id="bcss_stretch"></a><dl>
<dt><b>BCSS_STRETCH</b></dt>
</dl>
</td>
<td width="60%">
Stretch glyph, but try to retain aspect ratio.

</td>
</tr>
</table>

### -field size

Type: <b><a href="/windows/win32/api/windef/ns-windef-size">SIZE</a></b>

A <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure that specifies the size of the glyph in <b>himlGlyph</b>.

## -remarks

The glyph is the image that appears on the part of the button that activates the dropdown list. By default, this is an inverted triangle. Multiple images can be added to the image list to provide different glyphs for different states of the button, such as hot and pressed.

## -see-also

<a href="/windows/desktop/Controls/buttons">Buttons Overview</a>