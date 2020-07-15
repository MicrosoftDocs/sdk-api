---
UID: NF:strmif.IDvdControl.MenuLanguageSelect
title: IDvdControl::MenuLanguageSelect (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Sets the displayed language for navigation menus.
helpviewer_keywords: ["IDvdControl interface [DirectShow]","MenuLanguageSelect method","IDvdControl.MenuLanguageSelect","IDvdControl::MenuLanguageSelect","IDvdControlMenuLanguageSelect","MenuLanguageSelect","MenuLanguageSelect method [DirectShow]","MenuLanguageSelect method [DirectShow]","IDvdControl interface","dshow.idvdcontrol_menulanguageselect","strmif/IDvdControl::MenuLanguageSelect"]
old-location: dshow\idvdcontrol_menulanguageselect.htm
tech.root: DirectShow
ms.assetid: 6b5c660c-3d3f-4f78-8eca-3a42982eb0ae
ms.date: 12/05/2018
ms.keywords: IDvdControl interface [DirectShow],MenuLanguageSelect method, IDvdControl.MenuLanguageSelect, IDvdControl::MenuLanguageSelect, IDvdControlMenuLanguageSelect, MenuLanguageSelect, MenuLanguageSelect method [DirectShow], MenuLanguageSelect method [DirectShow],IDvdControl interface, dshow.idvdcontrol_menulanguageselect, strmif/IDvdControl::MenuLanguageSelect
f1_keywords:
- strmif/IDvdControl.MenuLanguageSelect
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
- IDvdControl.MenuLanguageSelect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl::MenuLanguageSelect


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Sets the displayed language for navigation menus.




## -parameters




### -param Language

Value that specifies the new language.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method selects the default language for menus.

This method returns an error unless the domain is DVD_DOMAIN_Stop. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

Applications specify languages with standard Windows LCIDs.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>
 

 

