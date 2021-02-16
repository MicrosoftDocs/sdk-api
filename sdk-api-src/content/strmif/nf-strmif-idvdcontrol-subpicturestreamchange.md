---
UID: NF:strmif.IDvdControl.SubpictureStreamChange
title: IDvdControl::SubpictureStreamChange (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Selects the new subpicture stream and enables or disables it for display.
helpviewer_keywords: ["IDvdControl interface [DirectShow]","SubpictureStreamChange method","IDvdControl.SubpictureStreamChange","IDvdControl::SubpictureStreamChange","IDvdControlSubpictureStreamChange","SubpictureStreamChange","SubpictureStreamChange method [DirectShow]","SubpictureStreamChange method [DirectShow]","IDvdControl interface","dshow.idvdcontrol_subpicturestreamchange","strmif/IDvdControl::SubpictureStreamChange"]
old-location: dshow\idvdcontrol_subpicturestreamchange.htm
tech.root: dshow
ms.assetid: 527031fa-bab9-49f5-89b1-f0c5c5812a76
ms.date: 12/05/2018
ms.keywords: IDvdControl interface [DirectShow],SubpictureStreamChange method, IDvdControl.SubpictureStreamChange, IDvdControl::SubpictureStreamChange, IDvdControlSubpictureStreamChange, SubpictureStreamChange, SubpictureStreamChange method [DirectShow], SubpictureStreamChange method [DirectShow],IDvdControl interface, dshow.idvdcontrol_subpicturestreamchange, strmif/IDvdControl::SubpictureStreamChange
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
 - IDvdControl::SubpictureStreamChange
 - strmif/IDvdControl::SubpictureStreamChange
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
 - IDvdControl.SubpictureStreamChange
---

# IDvdControl::SubpictureStreamChange


## -description

<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Selects the new subpicture stream and enables or disables it for display.

## -parameters

### -param ulSubPicture

Value that specifies the source of the subpicture, which must be from 0 through 32, or 63.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0-31</td>
<td>Indicates that the stream is valid.</td>
</tr>
<tr>
<td>32</td>
<td>Enables you to toggle the display without changing the current stream (that is, change <i>bDisplay</i> without altering the current stream).</td>
</tr>
<tr>
<td>63</td>
<td>Indicates that the stream is the dummy stream.</td>
</tr>
</table>

### -param bDisplay

Value that specifies whether the subpicture is enabled; <b>TRUE</b> makes the subpicture visible and <b>FALSE</b> hides it.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, DVD_DOMAIN_Title, or DVD_DOMAIN_Stop. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>