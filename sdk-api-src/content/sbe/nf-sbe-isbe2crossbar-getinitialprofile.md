---
UID: NF:sbe.ISBE2Crossbar.GetInitialProfile
title: ISBE2Crossbar::GetInitialProfile (sbe.h)
description: Gets the initial profile that lists the media types that are present in the currently loaded WTV file.
helpviewer_keywords: ["GetInitialProfile","GetInitialProfile method [Microsoft TV Technologies]","GetInitialProfile method [Microsoft TV Technologies]","ISBE2Crossbar interface","ISBE2Crossbar interface [Microsoft TV Technologies]","GetInitialProfile method","ISBE2Crossbar.GetInitialProfile","ISBE2Crossbar::GetInitialProfile","mstv.isbe2crossbar_getinitialprofile","sbe/ISBE2Crossbar::GetInitialProfile"]
old-location: mstv\isbe2crossbar_getinitialprofile.htm
tech.root: mstv
ms.assetid: 6a4bec40-2c6d-49fb-8977-3c3db2b2b4df
ms.date: 12/05/2018
ms.keywords: GetInitialProfile, GetInitialProfile method [Microsoft TV Technologies], GetInitialProfile method [Microsoft TV Technologies],ISBE2Crossbar interface, ISBE2Crossbar interface [Microsoft TV Technologies],GetInitialProfile method, ISBE2Crossbar.GetInitialProfile, ISBE2Crossbar::GetInitialProfile, mstv.isbe2crossbar_getinitialprofile, sbe/ISBE2Crossbar::GetInitialProfile
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
 - ISBE2Crossbar::GetInitialProfile
 - sbe/ISBE2Crossbar::GetInitialProfile
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
 - ISBE2Crossbar.GetInitialProfile
---

# ISBE2Crossbar::GetInitialProfile


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the initial profile that lists the media types that are present in the currently loaded WTV file. The media types in the profile correspond to the active pins on a <a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filter at the time the currently loaded  WTV file is created. The profile is fixed per loaded WTV file and does not change while the filter has a WTV file loaded . However, if the crossbar  is not in default profile mode, you can call the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2crossbar-setoutputprofile">SetOutputProfile</a> method to set a new profile for the crossbar. To disable default profile mode, call the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2crossbar-enabledefaultmode">EnableDefaultMode</a> method without the DEF_MODE_PROFILE flag.

## -parameters

### -param ppProfile [out]

Receives a pointer to the <a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2mediatypeprofile">ISBE2MediaTypeProfile</a> interface that implements the profile.
          
          The caller is responsible for releasing this interface. You can use this pointer to create a custom profile that you pass to the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2crossbar-setoutputprofile">SetOutputProfile</a> method.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_POINTER</dt>
</dl>
</td>
<td width="60%">
Null pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_FAIL</dt>
</dl>
</td>
<td width="60%">
Empty initial profiles.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2crossbar">ISBE2Crossbar</a>



<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2mediatypeprofile">ISBE2MediaTypeProfile</a>



<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2spanningevent">ISBE2SpanningEvent </a>



<a href="/previous-versions/windows/desktop/mstv/stream-buffer-sink2-filter">Stream Buffer Sink2 Filter</a>