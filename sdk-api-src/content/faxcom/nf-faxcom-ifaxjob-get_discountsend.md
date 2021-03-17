---
UID: NF:faxcom.IFaxJob.get_DiscountSend
title: IFaxJob::get_DiscountSend (faxcom.h)
description: The IFaxJob::get_DiscountSend property is a Boolean value that indicates whether the fax server will transmit the fax job during the discount rate period. The discount period applies only to outgoing fax transmissions.
helpviewer_keywords: ["DiscountSend property [Fax Service]","DiscountSend property [Fax Service]","IFaxJob interface","IFaxJob interface [Fax Service]","DiscountSend property","IFaxJob.DiscountSend","IFaxJob.get_DiscountSend","IFaxJob::DiscountSend","IFaxJob::get_DiscountSend","_mfax_ifaxjob_get_discountsend","fax._mfax_ifaxjob_get_discountsend","fax._mfax_ifaxjob_mfax_ifaxjob_get_discountsend_cpp","faxcom/IFaxJob::DiscountSend","faxcom/IFaxJob::get_DiscountSend","get_DiscountSend"]
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_discountsend_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8h9g.htm
ms.date: 12/05/2018
ms.keywords: DiscountSend property [Fax Service], DiscountSend property [Fax Service],IFaxJob interface, IFaxJob interface [Fax Service],DiscountSend property, IFaxJob.DiscountSend, IFaxJob.get_DiscountSend, IFaxJob::DiscountSend, IFaxJob::get_DiscountSend, _mfax_ifaxjob_get_discountsend, fax._mfax_ifaxjob_get_discountsend, fax._mfax_ifaxjob_mfax_ifaxjob_get_discountsend_cpp, faxcom/IFaxJob::DiscountSend, faxcom/IFaxJob::get_DiscountSend, get_DiscountSend
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
 - IFaxJob::get_DiscountSend
 - faxcom/IFaxJob::get_DiscountSend
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
 - IFaxJob.DiscountSend
 - IFaxJob.get_DiscountSend
---

# IFaxJob::get_DiscountSend


## -description

The <b>IFaxJob::get_DiscountSend</b> property is a Boolean value that indicates whether the fax server will transmit the fax job during the discount rate period. The discount period applies only to outgoing fax transmissions. 

This property is read-only.

## -parameters

## -remarks

To determine the period during which the discount rate applies, you can use the following IFaxServer properties. 

<ul>
<li>
<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountratestartminute-vb">DiscountRateStartMinute</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountrateendminute-vb">DiscountRateEndMinute</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountratestarthour-vb">DiscountRateStartHour</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountrateendhour-vb">DiscountRateEndHour</a>
</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjob">IFaxJob</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjobs">IFaxJobs</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-fax-jobs">Managing Fax Jobs</a>