---
UID: NF:faxcom.IFaxServer.get_DiscountRateStartHour
title: IFaxServer::get_DiscountRateStartHour (faxcom.h)
description: Sets or retrieves the DiscountRateStartHour property for a FaxServer object. The DiscountRateStartHour property is a number that represents the hour the discount period begins. The discount period applies only to outgoing fax transmissions. (Get)
helpviewer_keywords: ["DiscountRateStartHour property [Fax Service]","DiscountRateStartHour property [Fax Service]","IFaxServer interface","IFaxServer interface [Fax Service]","DiscountRateStartHour property","IFaxServer.DiscountRateStartHour","IFaxServer.get_DiscountRateStartHour","IFaxServer.put_DiscountRateStartHour","IFaxServer::DiscountRateStartHour","IFaxServer::get_DiscountRateStartHour","IFaxServer::put_DiscountRateStartHour","_mfax_ifaxserver_get_discountratestarthour","fax._mfax_ifaxserver_client_mfax_ifaxserver_get_discountratestarthour_cpp","fax._mfax_ifaxserver_get_discountratestarthour","faxcom/IFaxServer::DiscountRateStartHour","faxcom/IFaxServer::get_DiscountRateStartHour","faxcom/IFaxServer::put_DiscountRateStartHour","get_DiscountRateStartHour"]
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_get_discountratestarthour_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0oc2.htm
ms.date: 12/05/2018
ms.keywords: DiscountRateStartHour property [Fax Service], DiscountRateStartHour property [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],DiscountRateStartHour property, IFaxServer.DiscountRateStartHour, IFaxServer.get_DiscountRateStartHour, IFaxServer.put_DiscountRateStartHour, IFaxServer::DiscountRateStartHour, IFaxServer::get_DiscountRateStartHour, IFaxServer::put_DiscountRateStartHour, _mfax_ifaxserver_get_discountratestarthour, fax._mfax_ifaxserver_client_mfax_ifaxserver_get_discountratestarthour_cpp, fax._mfax_ifaxserver_get_discountratestarthour, faxcom/IFaxServer::DiscountRateStartHour, faxcom/IFaxServer::get_DiscountRateStartHour, faxcom/IFaxServer::put_DiscountRateStartHour, get_DiscountRateStartHour
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
 - IFaxServer::get_DiscountRateStartHour
 - faxcom/IFaxServer::get_DiscountRateStartHour
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
 - IFaxServer.DiscountRateStartHour
 - IFaxServer.get_DiscountRateStartHour
 - IFaxServer.put_DiscountRateStartHour
 - IFaxServer.get_DiscountRateStartHour
 - IFaxServer.put_DiscountRateStartHour
---

# IFaxServer::get_DiscountRateStartHour


## -description

Sets or retrieves the <b>DiscountRateStartHour</b> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>DiscountRateStartHour</b> property is a number that represents the hour the discount period begins. The discount period applies only to outgoing fax transmissions. 

This property is read/write.

## -parameters

## -remarks

To save on transmission costs, a user can queue a fax job and request that the fax server send the transmission during the discount rate period. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-discountsend-vb">IFaxDoc::DiscountSend Property</a>.
			

The <b>DiscountRateStartHour</b>, <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountratestartminute-vb">DiscountRateStartMinute</a>, <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountrateendhour-vb">DiscountRateEndHour</a>, and <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountrateendminute-vb">DiscountRateEndMinute</a> properties represent local time.
			

If the time the discount rate period ends is less than the time the discount rate period begins, the discount rate period extends into the next day. For example, if the discount rate period begins at 9:00 P.M. and ends at 7:00 A.M., the discount rate period begins in the evening and continues until the morning of the following day.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-discountsend-vb">DiscountSend</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountrateendhour-vb">IFaxServer::get_DiscountRateEndHour</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountrateendminute-vb">IFaxServer::get_DiscountRateEndMinute</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountratestartminute-vb">IFaxServer::get_DiscountRateStartMinute</a>
