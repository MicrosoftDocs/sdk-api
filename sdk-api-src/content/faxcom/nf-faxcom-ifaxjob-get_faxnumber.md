---
UID: NF:faxcom.IFaxJob.get_FaxNumber
title: IFaxJob::get_FaxNumber (faxcom.h)
description: The IFaxJob::get_FaxNumber property is a null-terminated string that contains the fax number to which the fax server will transmit the fax job. The IFaxJob::get_FaxNumber property applies only to outgoing fax transmissions.
helpviewer_keywords: ["FaxNumber property [Fax Service]","FaxNumber property [Fax Service]","IFaxJob interface","IFaxJob interface [Fax Service]","FaxNumber property","IFaxJob.FaxNumber","IFaxJob.get_FaxNumber","IFaxJob::FaxNumber","IFaxJob::get_FaxNumber","_mfax_ifaxjob_get_faxnumber","fax._mfax_ifaxjob_get_faxnumber","fax._mfax_ifaxjob_mfax_ifaxjob_get_faxnumber_cpp","faxcom/IFaxJob::FaxNumber","faxcom/IFaxJob::get_FaxNumber","get_FaxNumber"]
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_faxnumber_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_42wi.htm
ms.date: 12/05/2018
ms.keywords: FaxNumber property [Fax Service], FaxNumber property [Fax Service],IFaxJob interface, IFaxJob interface [Fax Service],FaxNumber property, IFaxJob.FaxNumber, IFaxJob.get_FaxNumber, IFaxJob::FaxNumber, IFaxJob::get_FaxNumber, _mfax_ifaxjob_get_faxnumber, fax._mfax_ifaxjob_get_faxnumber, fax._mfax_ifaxjob_mfax_ifaxjob_get_faxnumber_cpp, faxcom/IFaxJob::FaxNumber, faxcom/IFaxJob::get_FaxNumber, get_FaxNumber
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
 - IFaxJob::get_FaxNumber
 - faxcom/IFaxJob::get_FaxNumber
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
 - IFaxJob.FaxNumber
 - IFaxJob.get_FaxNumber
---

# IFaxJob::get_FaxNumber


## -description

The <b>IFaxJob::get_FaxNumber</b> property is a null-terminated string that contains the fax number to which the fax server will transmit the fax job. The <b>IFaxJob::get_FaxNumber</b> property applies only to outgoing fax transmissions.

This property is read-only.

## -parameters

## -remarks

A fax number is only available for faxes that have a <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxjob-get-type-vb">IFaxJob::get_Type</a> property equal to <b>JT_SEND</b>. If the fax number is not available, the <b>IFaxJob::get_FaxNumber</b> property contains an empty string.

<b>IFaxJob::get_FaxNumber</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjob">IFaxJob</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxjob-get-type-vb">IFaxJob::get_Type</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjobs">IFaxJobs</a>