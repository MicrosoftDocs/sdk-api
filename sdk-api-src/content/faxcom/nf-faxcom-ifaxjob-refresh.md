---
UID: NF:faxcom.IFaxJob.Refresh
title: IFaxJob::Refresh (faxcom.h)
description: The IFaxJob::Refresh method updates FaxJob object information for the associated fax job.
helpviewer_keywords: ["IFaxJob interface [Fax Service]","Refresh method","IFaxJob.Refresh","IFaxJob::Refresh","Refresh","Refresh method [Fax Service]","Refresh method [Fax Service]","IFaxJob interface","_mfax_ifaxjob_refresh","fax._mfax_ifaxjob_mfax_ifaxjob_refresh_cpp","fax._mfax_ifaxjob_refresh","faxcom/IFaxJob::Refresh"]
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7bqg.htm
ms.date: 12/05/2018
ms.keywords: IFaxJob interface [Fax Service],Refresh method, IFaxJob.Refresh, IFaxJob::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxJob interface, _mfax_ifaxjob_refresh, fax._mfax_ifaxjob_mfax_ifaxjob_refresh_cpp, fax._mfax_ifaxjob_refresh, faxcom/IFaxJob::Refresh
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
 - IFaxJob::Refresh
 - faxcom/IFaxJob::Refresh
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
 - IFaxJob.Refresh
 - IFaxJob.Refresh
---

# IFaxJob::Refresh


## -description

The <b>IFaxJob::Refresh</b> method updates <a href="/previous-versions/windows/desktop/fax/-mfax-faxjob">FaxJob</a> object information for the associated fax job.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call the <b>IFaxJob::Refresh</b> method to poll the fax service for new information about a specified fax job. After you successfully call <b>IFaxJob::Refresh</b>, you must call the appropriate <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjob">IFaxJob</a> interface method to retrieve new attribute values that are valid.

It is recommended that you limit calls to this method because frequent calls to <b>IFaxJob::Refresh</b> can degrade system performance.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjob">IFaxJob</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjobs">IFaxJobs</a>
