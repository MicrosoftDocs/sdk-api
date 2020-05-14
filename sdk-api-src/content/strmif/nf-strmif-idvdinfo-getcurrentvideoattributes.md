---
UID: NF:strmif.IDvdInfo.GetCurrentVideoAttributes
title: IDvdInfo::GetCurrentVideoAttributes (strmif.h)
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the current video attributes for the current title or menu.helpviewer_keywords: ["GetCurrentVideoAttributes","GetCurrentVideoAttributes method [DirectShow]","GetCurrentVideoAttributes method [DirectShow]","IDvdInfo interface","IDvdInfo interface [DirectShow]","GetCurrentVideoAttributes method","IDvdInfo.GetCurrentVideoAttributes","IDvdInfo::GetCurrentVideoAttributes","IDvdInfoGetCurrentVideoAttributes","dshow.idvdinfo_getcurrentvideoattributes","strmif/IDvdInfo::GetCurrentVideoAttributes"]
old-location: dshow\idvdinfo_getcurrentvideoattributes.htm
tech.root: DirectShow
ms.assetid: 7147d8f3-c038-4742-8667-2e40d7ab979a
ms.date: 12/05/2018
ms.keywords: GetCurrentVideoAttributes, GetCurrentVideoAttributes method [DirectShow], GetCurrentVideoAttributes method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetCurrentVideoAttributes method, IDvdInfo.GetCurrentVideoAttributes, IDvdInfo::GetCurrentVideoAttributes, IDvdInfoGetCurrentVideoAttributes, dshow.idvdinfo_getcurrentvideoattributes, strmif/IDvdInfo::GetCurrentVideoAttributes
f1_keywords:
- strmif/IDvdInfo.GetCurrentVideoAttributes
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
- IDvdInfo.GetCurrentVideoAttributes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdInfo::GetCurrentVideoAttributes


## -description



<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the current video attributes for the current title or menu.




## -parameters




### -param pATR [out]

Pointer to the retrieved video attributes.


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



This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

For information about DVD_VideoATR, see the DVD-Video specification.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo">IDvdInfo Interface</a>
 

 

