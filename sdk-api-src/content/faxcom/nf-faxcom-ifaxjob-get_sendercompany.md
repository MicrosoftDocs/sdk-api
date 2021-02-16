---
UID: NF:faxcom.IFaxJob.get_SenderCompany
title: IFaxJob::get_SenderCompany (faxcom.h)
description: The IFaxJob::get_SenderCompany property is a null-terminated string that contains the company name for the sender of the fax job. The IFaxJob::get_SenderCompany property applies only to outgoing fax transmissions.
helpviewer_keywords: ["IFaxJob interface [Fax Service]","SenderCompany property","IFaxJob.SenderCompany","IFaxJob.get_SenderCompany","IFaxJob::SenderCompany","IFaxJob::get_SenderCompany","SenderCompany property [Fax Service]","SenderCompany property [Fax Service]","IFaxJob interface","_mfax_ifaxjob_get_sendercompany","fax._mfax_ifaxjob_get_sendercompany","fax._mfax_ifaxjob_mfax_ifaxjob_get_sendercompany_cpp","faxcom/IFaxJob::SenderCompany","faxcom/IFaxJob::get_SenderCompany","get_SenderCompany"]
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_sendercompany_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7uk9.htm
ms.date: 12/05/2018
ms.keywords: IFaxJob interface [Fax Service],SenderCompany property, IFaxJob.SenderCompany, IFaxJob.get_SenderCompany, IFaxJob::SenderCompany, IFaxJob::get_SenderCompany, SenderCompany property [Fax Service], SenderCompany property [Fax Service],IFaxJob interface, _mfax_ifaxjob_get_sendercompany, fax._mfax_ifaxjob_get_sendercompany, fax._mfax_ifaxjob_mfax_ifaxjob_get_sendercompany_cpp, faxcom/IFaxJob::SenderCompany, faxcom/IFaxJob::get_SenderCompany, get_SenderCompany
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
 - IFaxJob::get_SenderCompany
 - faxcom/IFaxJob::get_SenderCompany
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
 - IFaxJob.SenderCompany
 - IFaxJob.get_SenderCompany
---

# IFaxJob::get_SenderCompany


## -description

The <b>IFaxJob::get_SenderCompany</b> property is a null-terminated string that contains the company name for the sender of the fax job. The <b>IFaxJob::get_SenderCompany</b> property applies only to outgoing fax transmissions.


This property is read-only.

## -parameters

## -remarks

If the sender's company is not available, the <b>IFaxJob::get_SenderCompany</b> property contains an empty string.

<b>IFaxJob::get_SenderCompany</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjob">IFaxJob</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjobs">IFaxJobs</a>