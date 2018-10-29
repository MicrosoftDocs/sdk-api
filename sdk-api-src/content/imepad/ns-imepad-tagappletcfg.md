---
UID: NS:imepad.tagAPPLETCFG
title: tagAPPLETCFG
author: windows-sdk-content
description: Used to specify and set applet configuration in IImePad.
old-location: intl\imeappletcfg.htm
tech.root: Intl
ms.assetid: 2680231A-0A9C-4723-8E7D-73184C209050
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*LPIMEAPPLETCFG, IMEAPPLETCFG, IMEAPPLETCFG structure [Internationalization for Windows Applications], IPACFG_CATEGORY, IPACFG_HELP, IPACFG_LANG, IPACFG_NONE, IPACFG_PROPERTY, IPACFG_TITLE, IPACFG_TITLEFONTFACE, PIMEAPPLETCFG, PIMEAPPLETCFG structure pointer [Internationalization for Windows Applications], imepad/IMEAPPLETCFG, imepad/PIMEAPPLETCFG, intl.imeappletcfg, tagAPPLETCFG"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Imepad.h
api_name:
 - IMEAPPLETCFG
product: Windows
targetos: Windows
req.typenames: IMEAPPLETCFG, *LPIMEAPPLETCFG
req.redist: 
---

# tagAPPLETCFG structure


## -description


Used to specify and set applet configuration in <a href="https://msdn.microsoft.com/6604112A-5BD5-4B2C-AECC-D09180B04D7F">IImePad</a>.


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
The applet has a property Dialog. If this flag is set, <a href="https://msdn.microsoft.com/6604112A-5BD5-4B2C-AECC-D09180B04D7F">IImePad</a> calls <a href="https://msdn.microsoft.com/5C370DC8-D308-4339-81F3-FEE88359A52F">IImePadApplet::Notify</a> with <b>IMEPN_CFG</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="IPACFG_HELP"></a><a id="ipacfg_help"></a><dl>
<dt><b>IPACFG_HELP</b></dt>
</dl>
</td>
<td width="60%">
The applet has help. If this flag is set, <a href="https://msdn.microsoft.com/6604112A-5BD5-4B2C-AECC-D09180B04D7F">IImePad</a> calls <a href="https://msdn.microsoft.com/5C370DC8-D308-4339-81F3-FEE88359A52F">IImePadApplet::Notify</a> with <b>IMEPN_HELP</b>.

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




<a href="https://msdn.microsoft.com/D24EF900-01D4-4E6E-B752-B11B2F4A6A6C">IImePadApplet::GetAppletCfg</a>
 

 

