---
UID: NF:strmif.IDvdInfo.GetVMGAttributes
title: IDvdInfo::GetVMGAttributes (strmif.h)
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves attributes of all video, audio, and subpicture streams for video manager (VMG) menus.
helpviewer_keywords: ["GetVMGAttributes","GetVMGAttributes method [DirectShow]","GetVMGAttributes method [DirectShow]","IDvdInfo interface","IDvdInfo interface [DirectShow]","GetVMGAttributes method","IDvdInfo.GetVMGAttributes","IDvdInfo::GetVMGAttributes","IDvdInfoGetVMGAttributes","dshow.idvdinfo_getvmgattributes","strmif/IDvdInfo::GetVMGAttributes"]
old-location: dshow\idvdinfo_getvmgattributes.htm
tech.root: dshow
ms.assetid: 449e7139-ed9f-46de-ac92-d1d67757799b
ms.date: 12/05/2018
ms.keywords: GetVMGAttributes, GetVMGAttributes method [DirectShow], GetVMGAttributes method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetVMGAttributes method, IDvdInfo.GetVMGAttributes, IDvdInfo::GetVMGAttributes, IDvdInfoGetVMGAttributes, dshow.idvdinfo_getvmgattributes, strmif/IDvdInfo::GetVMGAttributes
req.header: strmif.h
req.include-header: Dshow.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdInfo::GetVMGAttributes
 - strmif/IDvdInfo::GetVMGAttributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IDvdInfo.GetVMGAttributes
---

# IDvdInfo::GetVMGAttributes


## -description

<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves attributes of all video, audio, and subpicture streams for video manager (VMG) menus.

## -parameters

### -param pATR [out]

Pointer to the retrieved attributes structure.

## -returns

Returns an <b>HRESULT</b> value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
DVD is not initialized or domain is not DVD_DOMAIN_Title.

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
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
Requested action is not supported on this domain (<a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
Requested action cannot occur at this point in the movie due to the authoring of the current DVD-Video disc.

</td>
</tr>
</table>

## -remarks

This method is valid in any domain. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

The video manager contains a separate group of streams, such as the DVD_MENU_Title menus (see [DVD_MENU_ID](/windows/desktop/api/strmif/ne-strmif-dvd_menu_id)), and the streams are not associated with any particular title number.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo">IDvdInfo Interface</a>