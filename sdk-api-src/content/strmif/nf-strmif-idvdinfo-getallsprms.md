---
UID: NF:strmif.IDvdInfo.GetAllSPRMs
title: IDvdInfo::GetAllSPRMs (strmif.h)
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the current contents of all system parameter registers (SPRMs).
helpviewer_keywords: ["GetAllSPRMs","GetAllSPRMs method [DirectShow]","GetAllSPRMs method [DirectShow]","IDvdInfo interface","IDvdInfo interface [DirectShow]","GetAllSPRMs method","IDvdInfo.GetAllSPRMs","IDvdInfo::GetAllSPRMs","IDvdInfoGetAllSPRMs","dshow.idvdinfo_getallsprms","strmif/IDvdInfo::GetAllSPRMs"]
old-location: dshow\idvdinfo_getallsprms.htm
tech.root: dshow
ms.assetid: c96e0e7c-eee3-47ca-9350-94db895f1c6c
ms.date: 12/05/2018
ms.keywords: GetAllSPRMs, GetAllSPRMs method [DirectShow], GetAllSPRMs method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetAllSPRMs method, IDvdInfo.GetAllSPRMs, IDvdInfo::GetAllSPRMs, IDvdInfoGetAllSPRMs, dshow.idvdinfo_getallsprms, strmif/IDvdInfo::GetAllSPRMs
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
 - IDvdInfo::GetAllSPRMs
 - strmif/IDvdInfo::GetAllSPRMs
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
 - IDvdInfo.GetAllSPRMs
---

# IDvdInfo::GetAllSPRMs


## -description

<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the current contents of all system parameter registers (SPRMs).

## -parameters

### -param pRegisterArray [out]

Pointer to the retrieved array of system parameter registers.

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

For use of individual registers, see the DVD-Video specification.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo">IDvdInfo Interface</a>