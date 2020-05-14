---
UID: NF:strmif.IDvdControl.MenuCall
title: IDvdControl::MenuCall (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Displays the specified menu on the screen.helpviewer_keywords: ["IDvdControl interface [DirectShow]","MenuCall method","IDvdControl.MenuCall","IDvdControl::MenuCall","IDvdControlMenuCall","MenuCall","MenuCall method [DirectShow]","MenuCall method [DirectShow]","IDvdControl interface","dshow.idvdcontrol_menucall","strmif/IDvdControl::MenuCall"]
old-location: dshow\idvdcontrol_menucall.htm
tech.root: DirectShow
ms.assetid: b0e27b7a-cf14-4b4c-849e-0fa7f6b1c0ed
ms.date: 12/05/2018
ms.keywords: IDvdControl interface [DirectShow],MenuCall method, IDvdControl.MenuCall, IDvdControl::MenuCall, IDvdControlMenuCall, MenuCall, MenuCall method [DirectShow], MenuCall method [DirectShow],IDvdControl interface, dshow.idvdcontrol_menucall, strmif/IDvdControl::MenuCall
f1_keywords:
- strmif/IDvdControl.MenuCall
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
- IDvdControl.MenuCall
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl::MenuCall


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Displays the specified menu on the screen.




## -parameters




### -param MenuID [in]

Value that specifies the menu to display. Member of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-dvd_menu_id">DVD_MENU_ID</a> enumerated data type.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, DVD_DOMAIN_Title, or DVD_DOMAIN_Stop. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>
 

 

