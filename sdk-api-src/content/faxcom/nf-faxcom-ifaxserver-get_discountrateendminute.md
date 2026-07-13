---
UID: NF:faxcom.IFaxServer.get_DiscountRateEndMinute
title: IFaxServer::get_DiscountRateEndMinute (faxcom.h)
description: Sets or retrieves the DiscountRateEndMinute property for a FaxServer object. The DiscountRateEndMinute property is a number that represents the minute the discount period ends. The discount period applies only to outgoing fax transmissions. (Get)
helpviewer_keywords: ["DiscountRateEndMinute property [Fax Service]","DiscountRateEndMinute property [Fax Service]","IFaxServer interface","IFaxServer interface [Fax Service]","DiscountRateEndMinute property","IFaxServer.DiscountRateEndMinute","IFaxServer.get_DiscountRateEndMinute","IFaxServer.put_DiscountRateEndMinute","IFaxServer::DiscountRateEndMinute","IFaxServer::get_DiscountRateEndMinute","IFaxServer::put_DiscountRateEndMinute","_mfax_ifaxserver_get_discountrateendminute","fax._mfax_ifaxserver_client_mfax_ifaxserver_get_discountrateendminute_cpp","fax._mfax_ifaxserver_get_discountrateendminute","faxcom/IFaxServer::DiscountRateEndMinute","faxcom/IFaxServer::get_DiscountRateEndMinute","faxcom/IFaxServer::put_DiscountRateEndMinute","get_DiscountRateEndMinute"]
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_get_discountrateendminute_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1o4l.htm
ms.date: 12/05/2018
ms.keywords: DiscountRateEndMinute property [Fax Service], DiscountRateEndMinute property [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],DiscountRateEndMinute property, IFaxServer.DiscountRateEndMinute, IFaxServer.get_DiscountRateEndMinute, IFaxServer.put_DiscountRateEndMinute, IFaxServer::DiscountRateEndMinute, IFaxServer::get_DiscountRateEndMinute, IFaxServer::put_DiscountRateEndMinute, _mfax_ifaxserver_get_discountrateendminute, fax._mfax_ifaxserver_client_mfax_ifaxserver_get_discountrateendminute_cpp, fax._mfax_ifaxserver_get_discountrateendminute, faxcom/IFaxServer::DiscountRateEndMinute, faxcom/IFaxServer::get_DiscountRateEndMinute, faxcom/IFaxServer::put_DiscountRateEndMinute, get_DiscountRateEndMinute
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
 - IFaxServer::get_DiscountRateEndMinute
 - faxcom/IFaxServer::get_DiscountRateEndMinute
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
 - IFaxServer.DiscountRateEndMinute
 - IFaxServer.get_DiscountRateEndMinute
 - IFaxServer.put_DiscountRateEndMinute
 - IFaxServer.get_DiscountRateEndMinute
 - IFaxServer.put_DiscountRateEndMinute
---

# IFaxServer::get_DiscountRateEndMinute


## -description

Sets or retrieves the <b>DiscountRateEndMinute</b> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>DiscountRateEndMinute</b> property is a number that represents the minute the discount period ends. The discount period applies only to outgoing fax transmissions.

This property is read/write.

## -parameters

## -remarks

To save on transmission costs, a user can queue a fax job and request that the fax server send the transmission during the discount rate period. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-discountsend-vb">IFaxDoc::DiscountSend Property</a>.
			

The <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountratestarthour-vb">DiscountRateStartHour</a>, <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountratestartminute-vb">DiscountRateStartMinute</a>, <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountrateendhour-vb">DiscountRateEndHour</a>, and <b>DiscountRateEndMinute</b> properties represent local time.
			

If the time the discount rate period ends is less than the time the discount rate period begins, the discount rate period extends into the next day. For example, if the discount rate period begins at 9:00 P.M. and ends at 7:00 A.M., the discount rate period begins in the evening and continues until the morning of the following day.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-discountsend-vb">DiscountSend</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountrateendhour-vb">IFaxServer::get_DiscountRateEndHour</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountratestarthour-vb">IFaxServer::get_DiscountRateStartHour</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountratestartminute-vb">IFaxServer::get_DiscountRateStartMinute</a>
