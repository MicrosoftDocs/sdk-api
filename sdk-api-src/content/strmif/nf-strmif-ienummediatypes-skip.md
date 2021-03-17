---
UID: NF:strmif.IEnumMediaTypes.Skip
title: IEnumMediaTypes::Skip (strmif.h)
description: The Skip method skips over a specified number of media types.
helpviewer_keywords: ["IEnumMediaTypes interface [DirectShow]","Skip method","IEnumMediaTypes.Skip","IEnumMediaTypes::Skip","IEnumMediaTypesSkip","Skip","Skip method [DirectShow]","Skip method [DirectShow]","IEnumMediaTypes interface","dshow.ienummediatypes_skip","strmif/IEnumMediaTypes::Skip"]
old-location: dshow\ienummediatypes_skip.htm
tech.root: dshow
ms.assetid: 313628d0-256c-4142-bba5-7cd0c910610c
ms.date: 12/05/2018
ms.keywords: IEnumMediaTypes interface [DirectShow],Skip method, IEnumMediaTypes.Skip, IEnumMediaTypes::Skip, IEnumMediaTypesSkip, Skip, Skip method [DirectShow], Skip method [DirectShow],IEnumMediaTypes interface, dshow.ienummediatypes_skip, strmif/IEnumMediaTypes::Skip
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
 - IEnumMediaTypes::Skip
 - strmif/IEnumMediaTypes::Skip
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
 - IEnumMediaTypes.Skip
---

# IEnumMediaTypes::Skip


## -description

The <code>Skip</code> method skips over a specified number of media types.

## -parameters

### -param cMediaTypes [in]

Number of media types to skip.

## -returns

Returns one of the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Skipped past the end of the sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_ENUM_OUT_OF_SYNC</b></dt>
</dl>
</td>
<td width="60%">
The pin's state has changed and is now inconsistent with the enumerator.

</td>
</tr>
</table>

## -remarks

If the set of media types changes, the enumerator is no longer consistent with the pin, and the method returns VFW_E_ENUM_OUT_OF_SYNC. Discard any data obtained from previous calls to the enumerator, because it might be invalid. Update the enumerator by calling the <a href="/windows/desktop/api/strmif/nf-strmif-ienummediatypes-reset">IEnumMediaTypes::Reset</a> method. You can then call the <code>Skip</code> method safely.

## -see-also

<a href="/windows/desktop/DirectShow/enumerating-media-types">Enumerating Media Types</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ienummediatypes">IEnumMediaTypes Interface</a>