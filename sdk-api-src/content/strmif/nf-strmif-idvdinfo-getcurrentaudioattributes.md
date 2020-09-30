---
UID: NF:strmif.IDvdInfo.GetCurrentAudioAttributes
title: IDvdInfo::GetCurrentAudioAttributes (strmif.h)
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the attributes for the current audio stream in the current title or menu.
helpviewer_keywords: ["GetCurrentAudioAttributes","GetCurrentAudioAttributes method [DirectShow]","GetCurrentAudioAttributes method [DirectShow]","IDvdInfo interface","IDvdInfo interface [DirectShow]","GetCurrentAudioAttributes method","IDvdInfo.GetCurrentAudioAttributes","IDvdInfo::GetCurrentAudioAttributes","IDvdInfoGetCurrentAudioAttributes","dshow.idvdinfo_getcurrentaudioattributes","strmif/IDvdInfo::GetCurrentAudioAttributes"]
old-location: dshow\idvdinfo_getcurrentaudioattributes.htm
tech.root: dshow
ms.assetid: b6cb0162-747a-468d-a28f-49621dd27df0
ms.date: 12/05/2018
ms.keywords: GetCurrentAudioAttributes, GetCurrentAudioAttributes method [DirectShow], GetCurrentAudioAttributes method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetCurrentAudioAttributes method, IDvdInfo.GetCurrentAudioAttributes, IDvdInfo::GetCurrentAudioAttributes, IDvdInfoGetCurrentAudioAttributes, dshow.idvdinfo_getcurrentaudioattributes, strmif/IDvdInfo::GetCurrentAudioAttributes
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
 - IDvdInfo::GetCurrentAudioAttributes
 - strmif/IDvdInfo::GetCurrentAudioAttributes
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
 - IDvdInfo.GetCurrentAudioAttributes
---

# IDvdInfo::GetCurrentAudioAttributes


## -description

<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the attributes for the current audio stream in the current title or menu.

## -parameters

### -param pATR [out]

Pointer to the retrieved audio attributes.

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

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

For information about the DVD_AudioATR data type, consult the DVD-Video specification.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo">IDvdInfo Interface</a>