---
UID: NF:strmif.IEnumPins.Skip
title: IEnumPins::Skip (strmif.h)
description: The Skip method skips over a specified number of pins.
helpviewer_keywords: ["IEnumPins interface [DirectShow]","Skip method","IEnumPins.Skip","IEnumPins::Skip","IEnumPinsSkip","Skip","Skip method [DirectShow]","Skip method [DirectShow]","IEnumPins interface","dshow.ienumpins_skip","strmif/IEnumPins::Skip"]
old-location: dshow\ienumpins_skip.htm
tech.root: dshow
ms.assetid: 501d08ee-ebd1-48dc-8cc9-bf017034b4cd
ms.date: 12/05/2018
ms.keywords: IEnumPins interface [DirectShow],Skip method, IEnumPins.Skip, IEnumPins::Skip, IEnumPinsSkip, Skip, Skip method [DirectShow], Skip method [DirectShow],IEnumPins interface, dshow.ienumpins_skip, strmif/IEnumPins::Skip
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
 - IEnumPins::Skip
 - strmif/IEnumPins::Skip
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
 - IEnumPins.Skip
---

# IEnumPins::Skip


## -description

The <code>Skip</code> method skips over a specified number of pins.

## -parameters

### -param cPins [in]

Number of pins to skip.

## -returns

Returns one of the following <b>HRESULT</b>

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
The filter's state has changed and is now inconsistent with the enumerator.

</td>
</tr>
</table>

## -remarks

If the number of pins changes, the enumerator is no longer consistent with the filter, and the method returns VFW_E_ENUM_OUT_OF_SYNC. Discard any data obtained from previous calls to the enumerator, because it might be invalid. Update the enumerator by calling the <a href="/windows/desktop/api/strmif/nf-strmif-ienumpins-reset">IEnumPins::Reset</a> method. You can then call the <code>Skip</code> method safely.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ienumpins">IEnumPins Interface</a>