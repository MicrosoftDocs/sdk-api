---
UID: NS:uxtheme._BP_PAINTPARAMS
title: BP_PAINTPARAMS (uxtheme.h)
description: Defines paint operation parameters for BeginBufferedPaint.
helpviewer_keywords: ["*PBP_PAINTPARAMS","BPPF_ERASE","BPPF_NOCLIP","BPPF_NONCLIENT","BP_PAINTPARAMS","BP_PAINTPARAMS structure [Windows Controls]","PBP_PAINTPARAMS","PBP_PAINTPARAMS structure pointer [Windows Controls]","_shell_BP_PAINTPARAMS","_shell_BP_PAINTPARAMS_cpp","controls.BP_PAINTPARAMS","controls._shell_BP_PAINTPARAMS","uxtheme/BP_PAINTPARAMS","uxtheme/PBP_PAINTPARAMS"]
old-location: controls\BP_PAINTPARAMS.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\structures\bp_paintparams.htm
ms.date: 12/05/2018
ms.keywords: '*PBP_PAINTPARAMS, BPPF_ERASE, BPPF_NOCLIP, BPPF_NONCLIENT, BP_PAINTPARAMS, BP_PAINTPARAMS structure [Windows Controls], PBP_PAINTPARAMS, PBP_PAINTPARAMS structure pointer [Windows Controls], _shell_BP_PAINTPARAMS, _shell_BP_PAINTPARAMS_cpp, controls.BP_PAINTPARAMS, controls._shell_BP_PAINTPARAMS, uxtheme/BP_PAINTPARAMS, uxtheme/PBP_PAINTPARAMS'
req.header: uxtheme.h
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
req.typenames: BP_PAINTPARAMS, *PBP_PAINTPARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BP_PAINTPARAMS
 - uxtheme/_BP_PAINTPARAMS
 - PBP_PAINTPARAMS
 - uxtheme/PBP_PAINTPARAMS
 - BP_PAINTPARAMS
 - uxtheme/BP_PAINTPARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uxtheme.h
api_name:
 - BP_PAINTPARAMS
---

# BP_PAINTPARAMS structure


## -description

Defines paint operation parameters for <a href="/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedpaint">BeginBufferedPaint</a>.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The size, in bytes, of this structure.

### -field dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

One or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BPPF_ERASE"></a><a id="bppf_erase"></a><dl>
<dt><b>BPPF_ERASE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Initialize the buffer to ARGB = {0, 0, 0, 0} during <a href="/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedpaint">BeginBufferedPaint</a>. This erases the previous contents of the buffer.



</td>
</tr>
<tr>
<td width="40%"><a id="BPPF_NOCLIP"></a><a id="bppf_noclip"></a><dl>
<dt><b>BPPF_NOCLIP</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Do not apply the clip region of the target DC to the double buffer. If this flag is not set and if the target DC is a window DC, then clipping due to overlapping windows is applied to the double buffer. 

</td>
</tr>
<tr>
<td width="40%"><a id="BPPF_NONCLIENT"></a><a id="bppf_nonclient"></a><dl>
<dt><b>BPPF_NONCLIENT</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
A non-client DC is being used.

</td>
</tr>
</table>

### -field prcExclude

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to exclusion <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure. This rectangle is excluded from the clipping region.  May be <b>NULL</b> for no exclusion rectangle.

### -field pBlendFunction

Type: <b>const <a href="/windows/desktop/api/wingdi/ns-wingdi-blendfunction">BLENDFUNCTION</a>*</b>

A pointer to <a href="/windows/desktop/api/wingdi/ns-wingdi-blendfunction">BLENDFUNCTION</a> structure, which controls blending by specifying the blending functions for source and destination bitmaps.  If <b>NULL</b>, the source buffer is copied to the destination with no blending.