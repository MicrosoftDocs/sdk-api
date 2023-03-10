---
UID: NF:faxcom.IFaxJob.get_BillingCode
title: IFaxJob::get_BillingCode (faxcom.h)
description: The IFaxJob::get_BillingCode property is a null-terminated string that contains an optional billing code that applies to the fax job.
helpviewer_keywords: ["BillingCode property [Fax Service]","BillingCode property [Fax Service]","IFaxJob interface","IFaxJob interface [Fax Service]","BillingCode property","IFaxJob.BillingCode","IFaxJob.get_BillingCode","IFaxJob::BillingCode","IFaxJob::get_BillingCode","_mfax_ifaxjob_get_billingcode","fax._mfax_ifaxjob_get_billingcode","fax._mfax_ifaxjob_mfax_ifaxjob_get_billingcode_cpp","faxcom/IFaxJob::BillingCode","faxcom/IFaxJob::get_BillingCode","get_BillingCode"]
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_billingcode_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_2ov9.htm
ms.date: 12/05/2018
ms.keywords: BillingCode property [Fax Service], BillingCode property [Fax Service],IFaxJob interface, IFaxJob interface [Fax Service],BillingCode property, IFaxJob.BillingCode, IFaxJob.get_BillingCode, IFaxJob::BillingCode, IFaxJob::get_BillingCode, _mfax_ifaxjob_get_billingcode, fax._mfax_ifaxjob_get_billingcode, fax._mfax_ifaxjob_mfax_ifaxjob_get_billingcode_cpp, faxcom/IFaxJob::BillingCode, faxcom/IFaxJob::get_BillingCode, get_BillingCode
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
 - IFaxJob::get_BillingCode
 - faxcom/IFaxJob::get_BillingCode
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
 - IFaxJob.BillingCode
 - IFaxJob.get_BillingCode
---

# IFaxJob::get_BillingCode


## -description

The <b>IFaxJob::get_BillingCode</b> property is a null-terminated string that contains an optional billing code that applies to the fax job.

This property is read-only.

## -parameters

## -remarks

If billing information is not available, the <b>IFaxJob::get_BillingCode</b> property contains an empty string.

<b>IFaxJob::get_BillingCode</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjob">IFaxJob</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjobs">IFaxJobs</a>