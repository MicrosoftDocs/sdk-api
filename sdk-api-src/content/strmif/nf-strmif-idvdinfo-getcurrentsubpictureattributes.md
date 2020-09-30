---
UID: NF:strmif.IDvdInfo.GetCurrentSubpictureAttributes
title: IDvdInfo::GetCurrentSubpictureAttributes (strmif.h)
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the attributes for the current subpicture stream in the current title or menu.
helpviewer_keywords: ["GetCurrentSubpictureAttributes","GetCurrentSubpictureAttributes method [DirectShow]","GetCurrentSubpictureAttributes method [DirectShow]","IDvdInfo interface","IDvdInfo interface [DirectShow]","GetCurrentSubpictureAttributes method","IDvdInfo.GetCurrentSubpictureAttributes","IDvdInfo::GetCurrentSubpictureAttributes","IDvdInfoGetCurrentSubpictureAttributes","dshow.idvdinfo_getcurrentsubpictureattributes","strmif/IDvdInfo::GetCurrentSubpictureAttributes"]
old-location: dshow\idvdinfo_getcurrentsubpictureattributes.htm
tech.root: dshow
ms.assetid: 9beb31e3-b3ff-4c7a-922f-9f1e9725ddde
ms.date: 12/05/2018
ms.keywords: GetCurrentSubpictureAttributes, GetCurrentSubpictureAttributes method [DirectShow], GetCurrentSubpictureAttributes method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetCurrentSubpictureAttributes method, IDvdInfo.GetCurrentSubpictureAttributes, IDvdInfo::GetCurrentSubpictureAttributes, IDvdInfoGetCurrentSubpictureAttributes, dshow.idvdinfo_getcurrentsubpictureattributes, strmif/IDvdInfo::GetCurrentSubpictureAttributes
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
 - IDvdInfo::GetCurrentSubpictureAttributes
 - strmif/IDvdInfo::GetCurrentSubpictureAttributes
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
 - IDvdInfo.GetCurrentSubpictureAttributes
---

# IDvdInfo::GetCurrentSubpictureAttributes


## -description

<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the attributes for the current subpicture stream in the current title or menu.

## -parameters

### -param pATR [out]

Pointer to the retrieved subpicture attributes.

## -returns

Returns an <b>HRESULT</b> value .

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
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
Requested action cannot occur at this point in the movie due to the authoring of the current DVD-Video disc.

</td>
</tr>
</table>

## -remarks

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

For information about DVD_SubpictureATR, see the DVD-Video specification.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo">IDvdInfo Interface</a>