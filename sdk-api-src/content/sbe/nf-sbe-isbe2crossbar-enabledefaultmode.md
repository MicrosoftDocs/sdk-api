---
UID: NF:sbe.ISBE2Crossbar.EnableDefaultMode
title: ISBE2Crossbar::EnableDefaultMode (sbe.h)
description: Enables or disables the profile default mode and stream default mode for a crossbar in a Stream Buffer Source filter.
helpviewer_keywords: ["EnableDefaultMode","EnableDefaultMode method [Microsoft TV Technologies]","EnableDefaultMode method [Microsoft TV Technologies]","ISBE2Crossbar interface","ISBE2Crossbar interface [Microsoft TV Technologies]","EnableDefaultMode method","ISBE2Crossbar.EnableDefaultMode","ISBE2Crossbar::EnableDefaultMode","mstv.isbe2crossbar_enabledefaultmode","sbe/ISBE2Crossbar::EnableDefaultMode"]
old-location: mstv\isbe2crossbar_enabledefaultmode.htm
tech.root: mstv
ms.assetid: 5038050b-319d-488a-9cea-a2fc59b90cc8
ms.date: 12/05/2018
ms.keywords: EnableDefaultMode, EnableDefaultMode method [Microsoft TV Technologies], EnableDefaultMode method [Microsoft TV Technologies],ISBE2Crossbar interface, ISBE2Crossbar interface [Microsoft TV Technologies],EnableDefaultMode method, ISBE2Crossbar.EnableDefaultMode, ISBE2Crossbar::EnableDefaultMode, mstv.isbe2crossbar_enabledefaultmode, sbe/ISBE2Crossbar::EnableDefaultMode
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISBE2Crossbar::EnableDefaultMode
 - sbe/ISBE2Crossbar::EnableDefaultMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbe.h
api_name:
 - ISBE2Crossbar.EnableDefaultMode
---

# ISBE2Crossbar::EnableDefaultMode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Enables or disables the profile default mode and stream default mode for a crossbar in a <a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filter.
    The <i>profile</i>  describes a set of media types that can be used to create out pins, one media type per output pin. The <i>stream mapping</i> describes the mappings between the streams within a WTV file and filter output pins.

 If you do not call the <b>EnableDefaultMode</b> method in your application, the crossbar uses a default profile and a default stream map. In this case, the crossbar is said to be in <i>profile default mode</i> and <i>stream default mode</i>, respectively. You can use the <b>EnableDefaultMode</b> method to disable either mode or both modes, so that you can specify custom profiles or stream mappings. You can also use an <code>EnableDefaultMode(FALSE)</code> call to disable both default modes.

## -parameters

### -param DefaultFlags [in]

Specifies the default modes for the crossbar. This can be any combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>DEF_MODE_PROFILE</dt>
</dl>
</td>
<td width="60%">
Enables profile default mode. The default profile is used, and you cannot specify custom profiles by calling the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2crossbar-setoutputprofile">SetOutputProfile</a> method. If you omit this flag, profile default mode is disabled  so that you can specify a custom output profile.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>DEF_MODE_STREAMS</dt>
</dl>
</td>
<td width="60%">
Enables stream default mode. The Stream Buffer Engine (SBE) handles the mapping between streams and output pins, and you cannot change these mappings by calling the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2streammap-mapstream">ISBE2StreamMap::MapStream</a> method. If you omit this flag, stream default mode is disabled, so that you can specify a custom mapping.

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

In stream default mode, SBE first checks the Windows Media Center TV settings to determine if a preferred language is set. If a preferred language is set:

<ul>
<li>If an audio stream in the preferred language exists, SBE outputs that audio stream.</li>
<li>If an audio stream in the preferred language does not exist, SBE outputs the default audio stream, which is set when the stream is captured.</li>
</ul>
If no preferred language is set, Windows Media Center is either not present or not configured. In this case:

<ul>
<li>If an audio stream in the language the operating system locale exists, SBE outputs that audio stream.</li>
<li>Otherwise, SBE outputs the default audio stream.</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2crossbar">ISBE2Crossbar</a>



<a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2crossbar-setoutputprofile">ISBE2Crossbar::SetOutputProfile</a>



<a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2streammap-mapstream">ISBE2StreamMap::MapStream</a>



<a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source Filter</a>