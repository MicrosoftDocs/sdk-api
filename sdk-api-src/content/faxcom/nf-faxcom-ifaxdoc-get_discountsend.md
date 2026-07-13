---
UID: NF:faxcom.IFaxDoc.get_DiscountSend
title: IFaxDoc::get_DiscountSend (faxcom.h)
description: Sets or retrieves the DiscountSend property for a FaxDoc object. The DiscountSend property is a Boolean value that indicates whether the fax server transmits faxes during the discount period. (Get)
helpviewer_keywords: ["DiscountSend property [Fax Service]","DiscountSend property [Fax Service]","IFaxDoc interface","IFaxDoc interface [Fax Service]","DiscountSend property","IFaxDoc.DiscountSend","IFaxDoc.get_DiscountSend","IFaxDoc::DiscountSend","IFaxDoc::get_DiscountSend","IFaxDoc::put_DiscountSend","_mfax_ifaxdoc_get_discountsend","fax._mfax_ifaxdoc_get_discountsend","fax._mfax_ifaxdoc_mfax_ifaxdoc_get_discountsend_cpp","faxcom/IFaxDoc::DiscountSend","faxcom/IFaxDoc::get_DiscountSend","faxcom/IFaxDoc::put_DiscountSend","get_DiscountSend"]
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_discountsend_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_2usk.htm
ms.date: 12/05/2018
ms.keywords: DiscountSend property [Fax Service], DiscountSend property [Fax Service],IFaxDoc interface, IFaxDoc interface [Fax Service],DiscountSend property, IFaxDoc.DiscountSend, IFaxDoc.get_DiscountSend, IFaxDoc::DiscountSend, IFaxDoc::get_DiscountSend, IFaxDoc::put_DiscountSend, _mfax_ifaxdoc_get_discountsend, fax._mfax_ifaxdoc_get_discountsend, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_discountsend_cpp, faxcom/IFaxDoc::DiscountSend, faxcom/IFaxDoc::get_DiscountSend, faxcom/IFaxDoc::put_DiscountSend, get_DiscountSend
req.header: faxcom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Faxcom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxDoc::get_DiscountSend
 - faxcom/IFaxDoc::get_DiscountSend
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxDoc.DiscountSend
 - IFaxDoc.get_DiscountSend
 - IFaxDoc.put_DiscountSend
---

# IFaxDoc::get_DiscountSend


## -description

Sets or retrieves the <b>DiscountSend</b> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>DiscountSend</b> property is a Boolean value that indicates whether the fax server transmits faxes during the discount period.

This property is read/write.

## -parameters

## -remarks

To determine the period during which the discount rate applies, you can call the following <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a> methods: <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountratestartminute-vb">DiscountRateStartMinute</a>, <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountrateendminute-vb">DiscountRateEndMinute</a>, <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountratestarthour-vb">DiscountRateStartHour</a>, and <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountrateendhour-vb">DiscountRateEndHour</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountrateendhour-vb">DiscountRateEndHour</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountrateendminute-vb">DiscountRateEndMinute</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountratestarthour-vb">DiscountRateStartHour</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountratestartminute-vb">DiscountRateStartMinute</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxdoc">IFaxDoc</a>
