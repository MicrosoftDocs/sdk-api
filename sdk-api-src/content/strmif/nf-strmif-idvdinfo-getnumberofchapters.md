---
UID: NF:strmif.IDvdInfo.GetNumberOfChapters
title: IDvdInfo::GetNumberOfChapters (strmif.h)
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the number of chapters that are defined for a given title.helpviewer_keywords: ["GetNumberOfChapters","GetNumberOfChapters method [DirectShow]","GetNumberOfChapters method [DirectShow]","IDvdInfo interface","IDvdInfo interface [DirectShow]","GetNumberOfChapters method","IDvdInfo.GetNumberOfChapters","IDvdInfo::GetNumberOfChapters","IDvdInfoGetNumberOfChapters","dshow.idvdinfo_getnumberofchapters","strmif/IDvdInfo::GetNumberOfChapters"]
old-location: dshow\idvdinfo_getnumberofchapters.htm
tech.root: DirectShow
ms.assetid: 65d36d1c-956f-480f-adbb-1682eafc9c93
ms.date: 12/05/2018
ms.keywords: GetNumberOfChapters, GetNumberOfChapters method [DirectShow], GetNumberOfChapters method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetNumberOfChapters method, IDvdInfo.GetNumberOfChapters, IDvdInfo::GetNumberOfChapters, IDvdInfoGetNumberOfChapters, dshow.idvdinfo_getnumberofchapters, strmif/IDvdInfo::GetNumberOfChapters
f1_keywords:
- strmif/IDvdInfo.GetNumberOfChapters
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
- IDvdInfo.GetNumberOfChapters
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdInfo::GetNumberOfChapters


## -description



<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the number of chapters that are defined for a given title.




## -parameters




### -param ulTitle [in]

Title for which to retrieve the number of chapters.


### -param pulNumberOfChapters [out]

Pointer to the retrieved number of chapters for the specified title.


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



This method is valid in any domain. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo">IDvdInfo Interface</a>
 

 

