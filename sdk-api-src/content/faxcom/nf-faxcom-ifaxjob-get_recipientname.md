---
UID: NF:faxcom.IFaxJob.get_RecipientName
title: IFaxJob::get_RecipientName (faxcom.h)
description: The IFaxJob::get_RecipientName property is a null-terminated string that contains the name of the recipient of the fax job.
helpviewer_keywords: ["IFaxJob interface [Fax Service]","RecipientName property","IFaxJob.RecipientName","IFaxJob.get_RecipientName","IFaxJob::RecipientName","IFaxJob::get_RecipientName","RecipientName property [Fax Service]","RecipientName property [Fax Service]","IFaxJob interface","_mfax_ifaxjob_get_recipientname","fax._mfax_ifaxjob_get_recipientname","fax._mfax_ifaxjob_mfax_ifaxjob_get_recipientname_cpp","faxcom/IFaxJob::RecipientName","faxcom/IFaxJob::get_RecipientName","get_RecipientName"]
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_recipientname_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5vvp.htm
ms.date: 12/05/2018
ms.keywords: IFaxJob interface [Fax Service],RecipientName property, IFaxJob.RecipientName, IFaxJob.get_RecipientName, IFaxJob::RecipientName, IFaxJob::get_RecipientName, RecipientName property [Fax Service], RecipientName property [Fax Service],IFaxJob interface, _mfax_ifaxjob_get_recipientname, fax._mfax_ifaxjob_get_recipientname, fax._mfax_ifaxjob_mfax_ifaxjob_get_recipientname_cpp, faxcom/IFaxJob::RecipientName, faxcom/IFaxJob::get_RecipientName, get_RecipientName
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
 - IFaxJob::get_RecipientName
 - faxcom/IFaxJob::get_RecipientName
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
 - IFaxJob.RecipientName
 - IFaxJob.get_RecipientName
---

# IFaxJob::get_RecipientName


## -description

The <b>IFaxJob::get_RecipientName</b> property is a null-terminated string that contains the name of the recipient of the fax job.

This property is read-only.

## -parameters

## -remarks

If the recipient's name is not available, the <b>IFaxJob::get_RecipientName</b> property contains an empty string.

<b>IFaxJob::get_RecipientName</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjob">IFaxJob</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjobs">IFaxJobs</a>