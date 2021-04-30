---
UID: NF:strmif.IAMOverlayFX.SetOverlayFX
title: IAMOverlayFX::SetOverlayFX (strmif.h)
description: The SetOverlayFX method applies the specified effects to the overlay surface.
helpviewer_keywords: ["IAMOverlayFX interface [DirectShow]","SetOverlayFX method","IAMOverlayFX.SetOverlayFX","IAMOverlayFX::SetOverlayFX","IAMOverlayFXSetOverlayFX","SetOverlayFX","SetOverlayFX method [DirectShow]","SetOverlayFX method [DirectShow]","IAMOverlayFX interface","dshow.iamoverlayfx_setoverlayfx","strmif/IAMOverlayFX::SetOverlayFX"]
old-location: dshow\iamoverlayfx_setoverlayfx.htm
tech.root: dshow
ms.assetid: 08e44f4e-924a-4a4d-9fc5-c13b3c21c038
ms.date: 12/05/2018
ms.keywords: IAMOverlayFX interface [DirectShow],SetOverlayFX method, IAMOverlayFX.SetOverlayFX, IAMOverlayFX::SetOverlayFX, IAMOverlayFXSetOverlayFX, SetOverlayFX, SetOverlayFX method [DirectShow], SetOverlayFX method [DirectShow],IAMOverlayFX interface, dshow.iamoverlayfx_setoverlayfx, strmif/IAMOverlayFX::SetOverlayFX
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IAMOverlayFX::SetOverlayFX
 - strmif/IAMOverlayFX::SetOverlayFX
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
 - IAMOverlayFX.SetOverlayFX
---

# IAMOverlayFX::SetOverlayFX


## -description

The <code>SetOverlayFX</code> method applies the specified effects to the overlay surface.

## -parameters

### -param dwOverlayFX [in]

Value specifying which effects to apply. The value must be a logical combination of flags from the <a href="/windows/desktop/api/strmif/ne-strmif-amoverlayfx">AMOVERLAYFX</a> enumeration, or the method returns E_INVALIDARG.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface. The DirectShow implementation may return one of the following values, or others not listed.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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
</table>

## -remarks

The application must call this method while the filter graph is running. The effects are applied immediately.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamoverlayfx">IAMOverlayFX Interface</a>