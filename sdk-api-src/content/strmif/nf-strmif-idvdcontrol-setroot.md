---
UID: NF:strmif.IDvdControl.SetRoot
title: IDvdControl::SetRoot (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Sets the root directory containing the DVD-Video volume.
helpviewer_keywords: ["IDvdControl interface [DirectShow]","SetRoot method","IDvdControl.SetRoot","IDvdControl::SetRoot","IDvdControlSetRoot","SetRoot","SetRoot method [DirectShow]","SetRoot method [DirectShow]","IDvdControl interface","dshow.idvdcontrol_setroot","strmif/IDvdControl::SetRoot"]
old-location: dshow\idvdcontrol_setroot.htm
tech.root: dshow
ms.assetid: 3068edc0-c052-4f44-9f62-453320af20a3
ms.date: 12/05/2018
ms.keywords: IDvdControl interface [DirectShow],SetRoot method, IDvdControl.SetRoot, IDvdControl::SetRoot, IDvdControlSetRoot, SetRoot, SetRoot method [DirectShow], SetRoot method [DirectShow],IDvdControl interface, dshow.idvdcontrol_setroot, strmif/IDvdControl::SetRoot
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
 - IDvdControl::SetRoot
 - strmif/IDvdControl::SetRoot
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
 - IDvdControl.SetRoot
---

# IDvdControl::SetRoot


## -description

<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Sets the root directory containing the DVD-Video volume.

## -parameters

### -param pszPath [in]

Pointer to the directory name to set as the root directory.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method returns an error unless the domain is DVD_DOMAIN_Stop. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

If you haven't set the root directory before calling <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-titleplay">IDvdControl::TitlePlay</a>, the first drive starting from C: that contains a VIDEO_TS directory in the top level directory will be used as the root.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>