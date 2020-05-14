---
UID: NF:strmif.IDvdInfo.GetCurrentSubpicture
title: IDvdInfo::GetCurrentSubpicture (strmif.h)
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the number of available subpicture streams, the currently selected subpicture stream number, and whether the subpicture display is disabled.helpviewer_keywords: ["GetCurrentSubpicture","GetCurrentSubpicture method [DirectShow]","GetCurrentSubpicture method [DirectShow]","IDvdInfo interface","IDvdInfo interface [DirectShow]","GetCurrentSubpicture method","IDvdInfo.GetCurrentSubpicture","IDvdInfo::GetCurrentSubpicture","IDvdInfoGetCurrentSubpicture","dshow.idvdinfo_getcurrentsubpicture","strmif/IDvdInfo::GetCurrentSubpicture"]
old-location: dshow\idvdinfo_getcurrentsubpicture.htm
tech.root: DirectShow
ms.assetid: 92731904-2fb7-4dc2-b77f-1c40a002c469
ms.date: 12/05/2018
ms.keywords: GetCurrentSubpicture, GetCurrentSubpicture method [DirectShow], GetCurrentSubpicture method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetCurrentSubpicture method, IDvdInfo.GetCurrentSubpicture, IDvdInfo::GetCurrentSubpicture, IDvdInfoGetCurrentSubpicture, dshow.idvdinfo_getcurrentsubpicture, strmif/IDvdInfo::GetCurrentSubpicture
f1_keywords:
- strmif/IDvdInfo.GetCurrentSubpicture
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmif.h
api_name:
- IDvdInfo.GetCurrentSubpicture
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdInfo::GetCurrentSubpicture


## -description



<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the number of available subpicture streams, the currently selected subpicture stream number, and whether the subpicture display is disabled.




## -parameters




### -param pulStreamsAvailable [out]

Pointer to the retrieved number of available subpicture streams.


### -param pulCurrentStream [out]

Pointer to the retrieved number of the currently selected subpicture stream.


### -param pIsDisabled [out]

Pointer to a value indicating whether the subpicture display is disabled.


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
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
Requested action is not supported on this domain (<a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>).

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



Subpicture streams authored as forcedly activated streams will be displayed even if the application has disabled subpicture display with the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-subpicturestreamchange">IDvdControl::SubpictureStreamChange</a> method.

This method returns an error unless the domain is DVD_DOMAIN_Title. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo">IDvdInfo Interface</a>
 

 

