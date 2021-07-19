---
UID: NF:strmif.IDvdControl.LowerButtonSelect
title: IDvdControl::LowerButtonSelect (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Selects the lower directional button from the displayed menu.
helpviewer_keywords: ["IDvdControl interface [DirectShow]","LowerButtonSelect method","IDvdControl.LowerButtonSelect","IDvdControl::LowerButtonSelect","IDvdControlLowerButtonSelect","LowerButtonSelect","LowerButtonSelect method [DirectShow]","LowerButtonSelect method [DirectShow]","IDvdControl interface","dshow.idvdcontrol_lowerbuttonselect","strmif/IDvdControl::LowerButtonSelect"]
old-location: dshow\idvdcontrol_lowerbuttonselect.htm
tech.root: dshow
ms.assetid: eba476a5-c949-4ce1-b296-314e36afc912
ms.date: 12/05/2018
ms.keywords: IDvdControl interface [DirectShow],LowerButtonSelect method, IDvdControl.LowerButtonSelect, IDvdControl::LowerButtonSelect, IDvdControlLowerButtonSelect, LowerButtonSelect, LowerButtonSelect method [DirectShow], LowerButtonSelect method [DirectShow],IDvdControl interface, dshow.idvdcontrol_lowerbuttonselect, strmif/IDvdControl::LowerButtonSelect
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
 - IDvdControl::LowerButtonSelect
 - strmif/IDvdControl::LowerButtonSelect
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
 - IDvdControl.LowerButtonSelect
---

# IDvdControl::LowerButtonSelect


## -description

<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Selects the lower directional button from the displayed menu.



## -returns

Returns an <b>HRESULT</b> value.

## -remarks

On physical or electronic remote control devices, there is often a group of four directional buttons used for certain types of operations (such as menu navigation). This method tells DirectShow that something (the user, probably) triggered the lower directional button.

Selecting a DVD button simply highlights the button but does not activate the button. Selecting is the Windows equivalent of tabbing to a button but not pressing the SPACEBAR or ENTER key. Activating is the Windows equivalent of pressing the SPACEBAR or ENTER key after tabbing to a button.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>
