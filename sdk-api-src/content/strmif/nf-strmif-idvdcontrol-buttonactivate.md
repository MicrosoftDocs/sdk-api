---
UID: NF:strmif.IDvdControl.ButtonActivate
title: IDvdControl::ButtonActivate (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Activates the selected button.
helpviewer_keywords: ["ButtonActivate","ButtonActivate method [DirectShow]","ButtonActivate method [DirectShow]","IDvdControl interface","IDvdControl interface [DirectShow]","ButtonActivate method","IDvdControl.ButtonActivate","IDvdControl::ButtonActivate","IDvdControlButtonActivate","dshow.idvdcontrol_buttonactivate","strmif/IDvdControl::ButtonActivate"]
old-location: dshow\idvdcontrol_buttonactivate.htm
tech.root: dshow
ms.assetid: 6a5ee6ed-2baa-45d6-a874-5df4e5c56841
ms.date: 12/05/2018
ms.keywords: ButtonActivate, ButtonActivate method [DirectShow], ButtonActivate method [DirectShow],IDvdControl interface, IDvdControl interface [DirectShow],ButtonActivate method, IDvdControl.ButtonActivate, IDvdControl::ButtonActivate, IDvdControlButtonActivate, dshow.idvdcontrol_buttonactivate, strmif/IDvdControl::ButtonActivate
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
 - IDvdControl::ButtonActivate
 - strmif/IDvdControl::ButtonActivate
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
 - IDvdControl.ButtonActivate
---

# IDvdControl::ButtonActivate


## -description

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl</a> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Activates the selected button.



## -returns

This method does not return a value.

## -remarks

Selecting a DVD button simply highlights the button but does not activate the button. Selecting is equivalent of tabbing to a button but not pressing the SPACEBAR or ENTER key. Activating is equivalent of pressing the SPACEBAR or ENTER key after tabbing to a button.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol-buttonselectandactivate">IDvdControl::ButtonSelectAndActivate</a>
