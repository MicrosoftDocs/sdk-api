---
UID: NF:strmif.IDvdControl.TopPGSearch
title: IDvdControl::TopPGSearch (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Halts playback of the current program and restarts playback of the current program within the program chain (PGC).
helpviewer_keywords: ["IDvdControl interface [DirectShow]","TopPGSearch method","IDvdControl.TopPGSearch","IDvdControl::TopPGSearch","IDvdControlTopPGSearch","TopPGSearch","TopPGSearch method [DirectShow]","TopPGSearch method [DirectShow]","IDvdControl interface","dshow.idvdcontrol_toppgsearch","strmif/IDvdControl::TopPGSearch"]
old-location: dshow\idvdcontrol_toppgsearch.htm
tech.root: dshow
ms.assetid: 35a621de-5110-4999-8475-ae84a4dc9ee1
ms.date: 12/05/2018
ms.keywords: IDvdControl interface [DirectShow],TopPGSearch method, IDvdControl.TopPGSearch, IDvdControl::TopPGSearch, IDvdControlTopPGSearch, TopPGSearch, TopPGSearch method [DirectShow], TopPGSearch method [DirectShow],IDvdControl interface, dshow.idvdcontrol_toppgsearch, strmif/IDvdControl::TopPGSearch
f1_keywords:
- strmif/IDvdControl.TopPGSearch
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
- IDvdControl.TopPGSearch
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl::TopPGSearch


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Halts playback of the current program and restarts playback of the current program within the program chain (PGC).




## -parameters






## -returns



Returns an <b>HRESULT</b> value .




## -remarks



A program is usually equivalent to a chapter, and a PGC is usually equivalent to a title. In the case of One_Sequential_PGC_Titles, each program is required to be a chapter and each title has only one PGC, but in other cases (especially with random/shuffle PGCs and parental blocks) there can be more than one program between chapters and there can be more than one PGC in a title.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>
 

 

