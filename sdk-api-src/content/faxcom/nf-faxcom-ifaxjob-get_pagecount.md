---
UID: NF:faxcom.IFaxJob.get_PageCount
title: IFaxJob::get_PageCount (faxcom.h)
description: The IFaxJob::get_PageCount property is a number that represents the total number of pages in a fax transmission. The IFaxJob::get_PageCount property applies only to outgoing fax transmissions.
helpviewer_keywords: ["IFaxJob interface [Fax Service]","PageCount property","IFaxJob.PageCount","IFaxJob.get_PageCount","IFaxJob::PageCount","IFaxJob::get_PageCount","PageCount property [Fax Service]","PageCount property [Fax Service]","IFaxJob interface","_mfax_ifaxjob_get_pagecount","fax._mfax_ifaxjob_get_pagecount","fax._mfax_ifaxjob_mfax_ifaxjob_get_pagecount_cpp","faxcom/IFaxJob::PageCount","faxcom/IFaxJob::get_PageCount","get_PageCount"]
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_pagecount_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0nlg.htm
ms.date: 12/05/2018
ms.keywords: IFaxJob interface [Fax Service],PageCount property, IFaxJob.PageCount, IFaxJob.get_PageCount, IFaxJob::PageCount, IFaxJob::get_PageCount, PageCount property [Fax Service], PageCount property [Fax Service],IFaxJob interface, _mfax_ifaxjob_get_pagecount, fax._mfax_ifaxjob_get_pagecount, fax._mfax_ifaxjob_mfax_ifaxjob_get_pagecount_cpp, faxcom/IFaxJob::PageCount, faxcom/IFaxJob::get_PageCount, get_PageCount
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
 - IFaxJob::get_PageCount
 - faxcom/IFaxJob::get_PageCount
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
 - IFaxJob.PageCount
 - IFaxJob.get_PageCount
---

# IFaxJob::get_PageCount


## -description

The <b>IFaxJob::get_PageCount</b> property is a number that represents the total number of pages in a fax transmission. The <b>IFaxJob::get_PageCount</b> property applies only to outgoing fax transmissions.

This property is read-only.

## -parameters

## -remarks

The total page count is only available for faxes where <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxjob-get-type-vb">IFaxJob::get_Type</a> returns JT_SEND. If the page count is not available, <b>IFaxJob::get_PageCount</b> returns zero.

The total page count is only available for faxes that have a <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxjob-get-type-vb">IFaxJob::get_Type</a> property equal to JT_SEND. If the page count is not available, the <b>IFaxJob::get_PageCount</b> property is zero.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjob">IFaxJob</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxjob-get-type-vb">IFaxJob::get_Type</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjobs">IFaxJobs</a>