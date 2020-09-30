---
UID: NS:imepad.tagAPPLETCFG
title: IMEAPPLETCFG (imepad.h)
description: Used to specify and set applet configuration in IImePad.
helpviewer_keywords: ["*LPIMEAPPLETCFG","IMEAPPLETCFG","IMEAPPLETCFG structure [Internationalization for Windows Applications]","IPACFG_CATEGORY","IPACFG_HELP","IPACFG_LANG","IPACFG_NONE","IPACFG_PROPERTY","IPACFG_TITLE","IPACFG_TITLEFONTFACE","PIMEAPPLETCFG","PIMEAPPLETCFG structure pointer [Internationalization for Windows Applications]","imepad/IMEAPPLETCFG","imepad/PIMEAPPLETCFG","intl.imeappletcfg"]
old-location: intl\imeappletcfg.htm
tech.root: Intl
ms.assetid: 2680231A-0A9C-4723-8E7D-73184C209050
ms.date: 12/05/2018
ms.keywords: '*LPIMEAPPLETCFG, IMEAPPLETCFG, IMEAPPLETCFG structure [Internationalization for Windows Applications], IPACFG_CATEGORY, IPACFG_HELP, IPACFG_LANG, IPACFG_NONE, IPACFG_PROPERTY, IPACFG_TITLE, IPACFG_TITLEFONTFACE, PIMEAPPLETCFG, PIMEAPPLETCFG structure pointer [Internationalization for Windows Applications], imepad/IMEAPPLETCFG, imepad/PIMEAPPLETCFG, intl.imeappletcfg'
req.header: imepad.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: IMEAPPLETCFG, *LPIMEAPPLETCFG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagAPPLETCFG
 - imepad/tagAPPLETCFG
 - LPIMEAPPLETCFG
 - imepad/LPIMEAPPLETCFG
 - IMEAPPLETCFG
 - imepad/IMEAPPLETCFG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Imepad.h
api_name:
 - IMEAPPLETCFG
---

# IMEAPPLETCFG structure


## -description

Used to specify and set applet configuration in <a href="/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a>.

## -struct-fields

### -field dwConfig

Combination of <b>IPACFG_*</b> flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IPACFG_NONE"></a><a id="ipacfg_none"></a><dl>
<dt><b>IPACFG_NONE</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="IPACFG_PROPERTY"></a><a id="ipacfg_property"></a><dl>
<dt><b>IPACFG_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The applet has a property Dialog. If this flag is set, <a href="/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a> calls <a href="/windows/desktop/api/imepad/nf-imepad-iimepadapplet-notify">IImePadApplet::Notify</a> with <b>IMEPN_CFG</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="IPACFG_HELP"></a><a id="ipacfg_help"></a><dl>
<dt><b>IPACFG_HELP</b></dt>
</dl>
</td>
<td width="60%">
The applet has help. If this flag is set, <a href="/windows/desktop/api/imepad/nn-imepad-iimepad">IImePad</a> calls <a href="/windows/desktop/api/imepad/nf-imepad-iimepadapplet-notify">IImePadApplet::Notify</a> with <b>IMEPN_HELP</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="IPACFG_TITLE"></a><a id="ipacfg_title"></a><dl>
<dt><b>IPACFG_TITLE</b></dt>
</dl>
</td>
<td width="60%">
<b>wchTitle</b> is set. 

</td>
</tr>
<tr>
<td width="40%"><a id="IPACFG_TITLEFONTFACE"></a><a id="ipacfg_titlefontface"></a><dl>
<dt><b>IPACFG_TITLEFONTFACE</b></dt>
</dl>
</td>
<td width="60%">
<b>wchTitleFontFace</b> and <b>dwCharSet</b> are set.

</td>
</tr>
<tr>
<td width="40%"><a id="IPACFG_CATEGORY"></a><a id="ipacfg_category"></a><dl>
<dt><b>IPACFG_CATEGORY</b></dt>
</dl>
</td>
<td width="60%">
<b>iCategory</b>  is set.

</td>
</tr>
<tr>
<td width="40%"><a id="IPACFG_LANG"></a><a id="ipacfg_lang"></a><dl>
<dt><b>IPACFG_LANG</b></dt>
</dl>
</td>
<td width="60%">
<b>LangID</b> is set.

</td>
</tr>
</table>

### -field wchTitle

The applet's title, in Unicode.

### -field wchTitleFontFace

The applet title's FontFace name.

### -field dwCharSet

The applet font's character set.

### -field iCategory

Not used.

### -field hIcon

The icon handle for the ImePad applet's menu.

### -field langID

The applet's language ID.

### -field dummy

Not used.

### -field lReserved1

Reserved.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/hh851787(v=vs.85)">IImePadApplet::GetAppletCfg</a>