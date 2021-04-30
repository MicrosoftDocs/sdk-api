---
UID: NF:faxcom.IFaxJob.get_SenderName
title: IFaxJob::get_SenderName (faxcom.h)
description: The IFaxJob::get_SenderName property is a null-terminated string that contains the name of the sender who initiated the fax job. The IFaxJob::get_SenderName property applies only to outgoing fax transmissions.
helpviewer_keywords: ["IFaxJob interface [Fax Service]","SenderName property","IFaxJob.SenderName","IFaxJob.get_SenderName","IFaxJob::SenderName","IFaxJob::get_SenderName","SenderName property [Fax Service]","SenderName property [Fax Service]","IFaxJob interface","_mfax_ifaxjob_get_sendername","fax._mfax_ifaxjob_get_sendername","fax._mfax_ifaxjob_mfax_ifaxjob_get_sendername_cpp","faxcom/IFaxJob::SenderName","faxcom/IFaxJob::get_SenderName","get_SenderName"]
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_sendername_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_2vj9.htm
ms.date: 12/05/2018
ms.keywords: IFaxJob interface [Fax Service],SenderName property, IFaxJob.SenderName, IFaxJob.get_SenderName, IFaxJob::SenderName, IFaxJob::get_SenderName, SenderName property [Fax Service], SenderName property [Fax Service],IFaxJob interface, _mfax_ifaxjob_get_sendername, fax._mfax_ifaxjob_get_sendername, fax._mfax_ifaxjob_mfax_ifaxjob_get_sendername_cpp, faxcom/IFaxJob::SenderName, faxcom/IFaxJob::get_SenderName, get_SenderName
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
 - IFaxJob::get_SenderName
 - faxcom/IFaxJob::get_SenderName
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
 - IFaxJob.SenderName
 - IFaxJob.get_SenderName
---

# IFaxJob::get_SenderName


## -description

The <b>IFaxJob::get_SenderName</b> property is a null-terminated string that contains the name of the sender who initiated the fax job. The <b>IFaxJob::get_SenderName</b> property applies only to outgoing fax transmissions.

This property is read-only.

## -parameters

## -remarks

If the sender's name is not available, the <b>IFaxJob::get_SenderName</b> property contains an empty string.

You can call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxjob-get-username-vb">IFaxJob::get_UserName</a> method to retrieve the name of the account that queued the fax job. 

<b>IFaxJob::get_SenderName</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjob">IFaxJob</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxjob-get-username-vb">IFaxJob::get_UserName</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjobs">IFaxJobs</a>