---
UID: NF:strmif.IPersistMediaPropertyBag.Save
title: IPersistMediaPropertyBag::Save (strmif.h)
description: The Save method saves properties from the filter into the media property bag.
helpviewer_keywords: ["IPersistMediaPropertyBag interface [DirectShow]","Save method","IPersistMediaPropertyBag.Save","IPersistMediaPropertyBag::Save","IPersistMediaPropertyBagSave","Save","Save method [DirectShow]","Save method [DirectShow]","IPersistMediaPropertyBag interface","dshow.ipersistmediapropertybag_save","strmif/IPersistMediaPropertyBag::Save"]
old-location: dshow\ipersistmediapropertybag_save.htm
tech.root: dshow
ms.assetid: 12c66650-31c1-40b8-9f3d-bc5553dbfa94
ms.date: 12/05/2018
ms.keywords: IPersistMediaPropertyBag interface [DirectShow],Save method, IPersistMediaPropertyBag.Save, IPersistMediaPropertyBag::Save, IPersistMediaPropertyBagSave, Save, Save method [DirectShow], Save method [DirectShow],IPersistMediaPropertyBag interface, dshow.ipersistmediapropertybag_save, strmif/IPersistMediaPropertyBag::Save
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
 - IPersistMediaPropertyBag::Save
 - strmif/IPersistMediaPropertyBag::Save
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
 - IPersistMediaPropertyBag.Save
---

# IPersistMediaPropertyBag::Save


## -description

The <code>Save</code> method saves properties from the filter into the media property bag.

## -parameters

### -param pPropBag [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-imediapropertybag">IMediaPropertyBag</a> interface of a media property bag created by the caller.

### -param fClearDirty [in]

Reserved. Can be any value.

### -param fSaveAllProperties [in]

Reserved. Can be any value.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following:

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_DATA)</b></dt>
</dl>
</td>
<td width="60%">
Invalid data.

</td>
</tr>
</table>

## -remarks

If you call this method on the <a href="/windows/desktop/DirectShow/avi-splitter-filter">AVI Splitter</a> filter or the <a href="/windows/desktop/DirectShow/wave-parser-filter">WAVE Parser</a>, the filter reads any INFO and DISP chunks from the file and stores them in the media property bag. You can use the <a href="/windows/desktop/api/strmif/nf-strmif-imediapropertybag-enumproperty">IMediaPropertyBag::EnumProperty</a> method to retrieve the chunks.

The <a href="/windows/desktop/DirectShow/avi-mux-filter">AVI Mux</a> filter does not implement this method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ipersistmediapropertybag">IPersistMediaPropertyBag Interface</a>