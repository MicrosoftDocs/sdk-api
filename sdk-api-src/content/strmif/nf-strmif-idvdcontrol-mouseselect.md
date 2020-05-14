---
UID: NF:strmif.IDvdControl.MouseSelect
title: IDvdControl::MouseSelect (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Selects a DVD button in response to mouse movement.helpviewer_keywords: ["IDvdControl interface [DirectShow]","MouseSelect method","IDvdControl.MouseSelect","IDvdControl::MouseSelect","IDvdControlMouseSelect","MouseSelect","MouseSelect method [DirectShow]","MouseSelect method [DirectShow]","IDvdControl interface","dshow.idvdcontrol_mouseselect","strmif/IDvdControl::MouseSelect"]
old-location: dshow\idvdcontrol_mouseselect.htm
tech.root: DirectShow
ms.assetid: c843bf51-ae05-4045-b517-52daeda6bc07
ms.date: 12/05/2018
ms.keywords: IDvdControl interface [DirectShow],MouseSelect method, IDvdControl.MouseSelect, IDvdControl::MouseSelect, IDvdControlMouseSelect, MouseSelect, MouseSelect method [DirectShow], MouseSelect method [DirectShow],IDvdControl interface, dshow.idvdcontrol_mouseselect, strmif/IDvdControl::MouseSelect
f1_keywords:
- strmif/IDvdControl.MouseSelect
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
- IDvdControl.MouseSelect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl::MouseSelect


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Selects a DVD button in response to mouse movement.




## -parameters




### -param point [in]

Specified point within the display window.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method is valid in any domain. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

This method checks the specified point within the display window to see if it is within a current DVD button's highlight rectangle. If it is, this method selects the button.

DVD buttons do not all necessarily have highlight rectangles. Button rectangles can overlap, and the rectangles do not always correspond to the visual representation of DVD buttons.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>
 

 

