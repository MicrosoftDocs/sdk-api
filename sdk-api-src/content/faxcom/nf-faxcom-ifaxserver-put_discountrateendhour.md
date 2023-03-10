---
UID: NF:faxcom.IFaxServer.put_DiscountRateEndHour
title: IFaxServer::put_DiscountRateEndHour (faxcom.h)
description: Sets or retrieves the DiscountRateEndHour property for a FaxServer object. The DiscountRateEndHour property is a number that represents the hour the discount period ends. The discount period applies only to outgoing fax transmissions. (Put)
helpviewer_keywords: ["DiscountRateEndHour property [Fax Service]","DiscountRateEndHour property [Fax Service]","IFaxServer interface","IFaxServer interface [Fax Service]","DiscountRateEndHour property","IFaxServer.DiscountRateEndHour","IFaxServer.get_DiscountRateEndHour","IFaxServer.put_DiscountRateEndHour","IFaxServer::DiscountRateEndHour","IFaxServer::get_DiscountRateEndHour","IFaxServer::put_DiscountRateEndHour","_mfax_ifaxserver_get_discountrateendhour","fax._mfax_ifaxserver_client_mfax_ifaxserver_get_discountrateendhour_cpp","fax._mfax_ifaxserver_get_discountrateendhour","faxcom/IFaxServer::DiscountRateEndHour","faxcom/IFaxServer::get_DiscountRateEndHour","faxcom/IFaxServer::put_DiscountRateEndHour","put_DiscountRateEndHour"]
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_get_discountrateendhour_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_2g4y.htm
ms.date: 12/05/2018
ms.keywords: DiscountRateEndHour property [Fax Service], DiscountRateEndHour property [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],DiscountRateEndHour property, IFaxServer.DiscountRateEndHour, IFaxServer.get_DiscountRateEndHour, IFaxServer.put_DiscountRateEndHour, IFaxServer::DiscountRateEndHour, IFaxServer::get_DiscountRateEndHour, IFaxServer::put_DiscountRateEndHour, _mfax_ifaxserver_get_discountrateendhour, fax._mfax_ifaxserver_client_mfax_ifaxserver_get_discountrateendhour_cpp, fax._mfax_ifaxserver_get_discountrateendhour, faxcom/IFaxServer::DiscountRateEndHour, faxcom/IFaxServer::get_DiscountRateEndHour, faxcom/IFaxServer::put_DiscountRateEndHour, put_DiscountRateEndHour
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
 - IFaxServer::put_DiscountRateEndHour
 - faxcom/IFaxServer::put_DiscountRateEndHour
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
 - IFaxServer.DiscountRateEndHour
 - IFaxServer.get_DiscountRateEndHour
 - IFaxServer.put_DiscountRateEndHour
 - IFaxServer.get_DiscountRateEndHour
 - IFaxServer.put_DiscountRateEndHour
---

# IFaxServer::put_DiscountRateEndHour


## -description

Sets or retrieves the <b>DiscountRateEndHour</b> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>DiscountRateEndHour</b> property is a number that represents the hour the discount period ends. The discount period applies only to outgoing fax transmissions.

This property is read/write.

## -parameters

## -remarks

To save on transmission costs, a user can queue a fax job and request that the fax server send the transmission during the discount rate period. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-discountsend-vb">IFaxDoc::DiscountSend Property</a>.
			

The <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountratestarthour-vb">DiscountRateStartHour</a>, <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountratestartminute-vb">DiscountRateStartMinute</a>, <b>DiscountRateEndHour</b>, and <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountrateendminute-vb">DiscountRateEndMinute</a> properties represent local time.
			

If the time the discount rate period ends is less than the time the discount rate period begins, the discount rate period extends into the next day. For example, if the discount rate period begins at 9:00 P.M. and ends at 7:00 A.M., the discount rate period begins in the evening and continues until the morning of the following day.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-discountsend-vb">DiscountSend</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountrateendminute-vb">IFaxServer::get_DiscountRateEndMinute</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountratestarthour-vb">IFaxServer::get_DiscountRateStartHour</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountratestartminute-vb">IFaxServer::get_DiscountRateStartMinute</a>
