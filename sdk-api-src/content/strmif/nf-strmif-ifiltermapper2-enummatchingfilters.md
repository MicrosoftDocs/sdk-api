---
UID: NF:strmif.IFilterMapper2.EnumMatchingFilters
title: IFilterMapper2::EnumMatchingFilters (strmif.h)
description: The EnumMatchingFilters method enumerates registered filters that meet specified requirements.
helpviewer_keywords: ["EnumMatchingFilters","EnumMatchingFilters method [DirectShow]","EnumMatchingFilters method [DirectShow]","IFilterMapper2 interface","IFilterMapper2 interface [DirectShow]","EnumMatchingFilters method","IFilterMapper2.EnumMatchingFilters","IFilterMapper2::EnumMatchingFilters","IFilterMapper2EnumMatchingFilters","dshow.ifiltermapper2_enummatchingfilters","strmif/IFilterMapper2::EnumMatchingFilters"]
old-location: dshow\ifiltermapper2_enummatchingfilters.htm
tech.root: dshow
ms.assetid: f121b4c3-fce1-4be3-ace4-5084242130f6
ms.date: 4/26/2023
ms.keywords: EnumMatchingFilters, EnumMatchingFilters method [DirectShow], EnumMatchingFilters method [DirectShow],IFilterMapper2 interface, IFilterMapper2 interface [DirectShow],EnumMatchingFilters method, IFilterMapper2.EnumMatchingFilters, IFilterMapper2::EnumMatchingFilters, IFilterMapper2EnumMatchingFilters, dshow.ifiltermapper2_enummatchingfilters, strmif/IFilterMapper2::EnumMatchingFilters
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFilterMapper2::EnumMatchingFilters
 - strmif/IFilterMapper2::EnumMatchingFilters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFilterMapper2.EnumMatchingFilters
---

# IFilterMapper2::EnumMatchingFilters


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>EnumMatchingFilters</code> method enumerates registered filters that meet specified requirements.

## -parameters

### -param ppEnum [out]

Receives a pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-ienummoniker">IEnumMoniker</a> interface. Use this interface pointer to retrieve filter monikers from the enumeration. The caller must release the interface.

### -param dwFlags [in]

Reserved, must be zero.

### -param bExactMatch [in]

Boolean value indicating whether an exact match is required. See Remarks for more information.

### -param dwMerit [in]

Minimum merit value. The enumeration excludes filters with a lesser merit value. For a list of merit values, see <a href="/windows/desktop/DirectShow/merit">Merit</a>. If <i>dwMerit</i> is higher than MERIT_DO_NOT_USE, the enumeration also excludes filters whose category has a merit less than or equal to MERIT_DO_NOT_USE. (See <a href="/windows/desktop/DirectShow/filter-categories">Filter Categories</a>.)

### -param bInputNeeded [in]

Boolean value indicating whether the filter must have an input pin. If the value is <b>TRUE</b>, the filter must have at least one input pin.

### -param cInputTypes [in]

Number of input media types specified in <i>pInputTypes</i>.

### -param pInputTypes [in]

Pointer to an array of GUID pairs that specify major types and subtypes, for the input pins to match. The size of the array is 2 * <i>cInputTypes</i>. The array can be <b>NULL</b>. Individual array members can be GUID_NULL, which matches any type. (See <a href="/windows/desktop/DirectShow/media-types">Media Types</a>.)

### -param pMedIn [in]

Pointer to a <a href="/windows/desktop/api/strmif/ns-strmif-regpinmedium">REGPINMEDIUM</a> structure specifying the medium for the input pins. Set to <b>NULL</b> if not needed.

### -param pPinCategoryIn [in]

Pointer to a GUID that specifies the input pin category. (See <a href="/windows/desktop/DirectShow/pin-property-set">Pin Property Set</a>.) Set to <b>NULL</b> if not needed.

### -param bRender [in]

Boolean value that specifies whether the filter must render its input. If <b>TRUE</b>, the specified filter must render its input. (This value corresponds to the <b>bRendered</b> field in the <a href="/windows/desktop/api/strmif/ns-strmif-regfilterpins">REGFILTERPINS</a> structure, which is used to register information about the filter's pins.)

### -param bOutputNeeded [in]

Boolean value specifying whether the filter must have an output pin. If <b>TRUE</b>, the filter must have at least one output pin.

### -param cOutputTypes [in]

Number of input media types specified in <i>pOutputTypes</i>.

### -param pOutputTypes [in]

Pointer to an array of GUID pairs that specify major types and subtypes, for the output pins to match. The size of the array is 2 * <i>cOutputTypes</i>. The array can be <b>NULL</b>. Individual array members can be GUID_NULL, which matches any type.

### -param pMedOut [in]

Pointer to a <a href="/windows/desktop/api/strmif/ns-strmif-regpinmedium">REGPINMEDIUM</a> structure specifying the medium for the output pins. Set to <b>NULL</b> if not needed.

### -param pPinCategoryOut [in]

Pointer to a GUID that specifies the output pin category. (See <a href="/windows/desktop/DirectShow/pin-property-set">Pin Property Set</a>.) Set to <b>NULL</b> if not needed.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
</table>

## -remarks

To find filters whose input pins match a given set of media types, declare an array with major-type GUIDs and subtype GUIDs ordered in pairs. Pass the array address in the <i>pInputTypes</i> parameter, and set the <i>cInputTypes</i> parameter equal to the number of pairs (that is, half the array size):

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
GUID arrayInTypes[2];
arrayInTypes[0] = MEDIATYPE_Video;
arrayInTypes[1] = GUID_NULL;

DWORD cInTypes = 1;
</pre>
</td>
</tr>
</table></span></div>
For output pins, pass a similar array in the <i>pOutputTypes</i> parameter, and specify the number of GUID pairs in the <i>cOutputTypes</i> parameter.

If the value of the <i>bExactMatch</i> parameter is <b>TRUE</b>, this method looks for filters that exactly match the values you specify for media type, pin category, and pin medium. If the value is <b>FALSE</b>, filters that register a value of <b>NULL</b> for any of these items are considered a match. (In effect, a <b>NULL</b> value in the registry acts as a wildcard.)

If you specify <b>NULL</b> for media type, pin category, or pin medium, any filter is considered a match for that parameter.

If a pin did not register any media types, this method will not consider it a match for the media type.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2 Interface</a>