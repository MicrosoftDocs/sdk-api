---
UID: NF:strmif.IDvdControl.AngleChange
title: IDvdControl::AngleChange (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Sets the new display angle.
helpviewer_keywords: ["AngleChange","AngleChange method [DirectShow]","AngleChange method [DirectShow]","IDvdControl interface","IDvdControl interface [DirectShow]","AngleChange method","IDvdControl.AngleChange","IDvdControl::AngleChange","IDvdControlAngleChange","dshow.idvdcontrol_anglechange","strmif/IDvdControl::AngleChange"]
old-location: dshow\idvdcontrol_anglechange.htm
tech.root: dshow
ms.assetid: 4a91f05d-1ded-4ecb-8850-5ee7faad134d
ms.date: 12/05/2018
ms.keywords: AngleChange, AngleChange method [DirectShow], AngleChange method [DirectShow],IDvdControl interface, IDvdControl interface [DirectShow],AngleChange method, IDvdControl.AngleChange, IDvdControl::AngleChange, IDvdControlAngleChange, dshow.idvdcontrol_anglechange, strmif/IDvdControl::AngleChange
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
 - IDvdControl::AngleChange
 - strmif/IDvdControl::AngleChange
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
 - IDvdControl.AngleChange
---

# IDvdControl::AngleChange


## -description

<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Sets the new display angle.

## -parameters

### -param ulAngle [in]

Value of the new angle, which must be from 1 through 9.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, DVD_DOMAIN_Title, or DVD_DOMAIN_Stop. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>