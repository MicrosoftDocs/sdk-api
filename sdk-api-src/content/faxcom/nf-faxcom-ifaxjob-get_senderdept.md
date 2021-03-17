---
UID: NF:faxcom.IFaxJob.get_SenderDept
title: IFaxJob::get_SenderDept (faxcom.h)
description: The IFaxJob::get_SenderDept property is a null-terminated string that contains the department identifier for the sender of the fax job. The IFaxJob::get_SenderDept property applies only to outgoing fax transmissions.
helpviewer_keywords: ["IFaxJob interface [Fax Service]","SenderDept property","IFaxJob.SenderDept","IFaxJob.get_SenderDept","IFaxJob::SenderDept","IFaxJob::get_SenderDept","SenderDept property [Fax Service]","SenderDept property [Fax Service]","IFaxJob interface","_mfax_ifaxjob_get_senderdept","fax._mfax_ifaxjob_get_senderdept","fax._mfax_ifaxjob_mfax_ifaxjob_get_senderdept_cpp","faxcom/IFaxJob::SenderDept","faxcom/IFaxJob::get_SenderDept","get_SenderDept"]
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_senderdept_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_71mc.htm
ms.date: 12/05/2018
ms.keywords: IFaxJob interface [Fax Service],SenderDept property, IFaxJob.SenderDept, IFaxJob.get_SenderDept, IFaxJob::SenderDept, IFaxJob::get_SenderDept, SenderDept property [Fax Service], SenderDept property [Fax Service],IFaxJob interface, _mfax_ifaxjob_get_senderdept, fax._mfax_ifaxjob_get_senderdept, fax._mfax_ifaxjob_mfax_ifaxjob_get_senderdept_cpp, faxcom/IFaxJob::SenderDept, faxcom/IFaxJob::get_SenderDept, get_SenderDept
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
 - IFaxJob::get_SenderDept
 - faxcom/IFaxJob::get_SenderDept
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
 - IFaxJob.SenderDept
 - IFaxJob.get_SenderDept
---

# IFaxJob::get_SenderDept


## -description

The <b>IFaxJob::get_SenderDept</b> property is a null-terminated string that contains the department identifier for the sender of the fax job. The <b>IFaxJob::get_SenderDept</b> property applies only to outgoing fax transmissions.

This property is read-only.

## -parameters

## -remarks

If the sender's department is not available, the <b>IFaxJob::get_SenderDept</b> property contains an empty string.

The <b>IFaxJob::get_SenderDept</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjob">IFaxJob</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjobs">IFaxJobs</a>