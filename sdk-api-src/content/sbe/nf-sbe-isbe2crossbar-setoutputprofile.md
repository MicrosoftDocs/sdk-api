---
UID: NF:sbe.ISBE2Crossbar.SetOutputProfile
title: ISBE2Crossbar::SetOutputProfile (sbe.h)
description: Replaces the default or current input profile with the profile specified in this method.
helpviewer_keywords: ["ISBE2Crossbar interface [Microsoft TV Technologies]","SetOutputProfile method","ISBE2Crossbar.SetOutputProfile","ISBE2Crossbar::SetOutputProfile","SetOutputProfile","SetOutputProfile method [Microsoft TV Technologies]","SetOutputProfile method [Microsoft TV Technologies]","ISBE2Crossbar interface","mstv.isbe2crossbar_setoutputprofile","sbe/ISBE2Crossbar::SetOutputProfile"]
old-location: mstv\isbe2crossbar_setoutputprofile.htm
tech.root: mstv
ms.assetid: 34067ca5-ead0-44ac-b274-dc9e3f2fb2fd
ms.date: 12/05/2018
ms.keywords: ISBE2Crossbar interface [Microsoft TV Technologies],SetOutputProfile method, ISBE2Crossbar.SetOutputProfile, ISBE2Crossbar::SetOutputProfile, SetOutputProfile, SetOutputProfile method [Microsoft TV Technologies], SetOutputProfile method [Microsoft TV Technologies],ISBE2Crossbar interface, mstv.isbe2crossbar_setoutputprofile, sbe/ISBE2Crossbar::SetOutputProfile
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
 - ISBE2Crossbar::SetOutputProfile
 - sbe/ISBE2Crossbar::SetOutputProfile
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
 - ISBE2Crossbar.SetOutputProfile
---

# ISBE2Crossbar::SetOutputProfile


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Replaces the default or current input profile with the profile specified in this method.
    

You can discover the current input profile by calling the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2crossbar-getinitialprofile">GetInitialProfile</a> method. This profile can be changed over time as media types are updated on input to the <a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filter.

A custom profile can contain only one stream per major media type. For example, a custom profile can contain only a single audio stream.

By default, the filter crossbar  has   profile default mode enabled, which means that you cannot set  a custom output profile. Before you can set a custom output profile, you must disable profile default mode by calling the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2crossbar-enabledefaultmode">EnableDefaultMode</a> method without the DEF_MODE_PROFILE flag.

## -parameters

### -param pProfile [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2mediatypeprofile">ISBE2MediaTypeProfile</a> interface for the profile that replaces the crossbar default profile.

### -param pcOutputPins [in, out]

On input, specifies the size of an array allocated to receive <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> pointers for the output pins that correspond to the streams in the new profile. The <i>ppOutputPins</i> parameter points to this array. On output, if the call succeeds, gets the actual number of <b>IPin</b> pointers returned in the <i>ppOutputPins</i> output parameter.

### -param ppOutputPins [in, out]

On input, specifies a pointer to an array of uninitialized <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> pointers. On output, if the call succeeds, the <b>IPin</b> pointers in the array are initialized to point to the filter output pins that have the media types listed in the new profile. The <i>pcOutputPins</i> parameter gives the number of elements in the array. The caller is responsible for freeing the <b>IPin</b> interface pointers returned in the array.

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
<dt>E_INVALIDARG</dt>
</dl>
</td>
<td width="60%">
The <i>pProfile</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_POINTER</dt>
</dl>
</td>
<td width="60%">
The <i>pcOutputPins</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_UNEXPECTED</dt>
</dl>
</td>
<td width="60%">
Cannot set output profile because profile default mode is enabled.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2crossbar-enabledefaultmode">EnableDefaultMode</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a>



<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2crossbar">ISBE2Crossbar</a>



<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2mediatypeprofile">ISBE2MediaTypeProfile </a>



<a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source Filter</a>