---
UID: NF:faxcom.IFaxJob.get_UserName
title: IFaxJob::get_UserName (faxcom.h)
description: The IFaxJob::get_UserName property is a null-terminated string that contains the name of the user who submitted the fax job to the job queue. The IFaxJob::get_UserName property applies only to outgoing fax transmissions.
helpviewer_keywords: ["IFaxJob interface [Fax Service]","UserName property","IFaxJob.UserName","IFaxJob.get_UserName","IFaxJob::UserName","IFaxJob::get_UserName","UserName property [Fax Service]","UserName property [Fax Service]","IFaxJob interface","_mfax_ifaxjob_get_username","fax._mfax_ifaxjob_get_username","fax._mfax_ifaxjob_mfax_ifaxjob_get_username_cpp","faxcom/IFaxJob::UserName","faxcom/IFaxJob::get_UserName","get_UserName"]
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_username_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6jad.htm
ms.date: 12/05/2018
ms.keywords: IFaxJob interface [Fax Service],UserName property, IFaxJob.UserName, IFaxJob.get_UserName, IFaxJob::UserName, IFaxJob::get_UserName, UserName property [Fax Service], UserName property [Fax Service],IFaxJob interface, _mfax_ifaxjob_get_username, fax._mfax_ifaxjob_get_username, fax._mfax_ifaxjob_mfax_ifaxjob_get_username_cpp, faxcom/IFaxJob::UserName, faxcom/IFaxJob::get_UserName, get_UserName
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
 - IFaxJob::get_UserName
 - faxcom/IFaxJob::get_UserName
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
 - IFaxJob.UserName
 - IFaxJob.get_UserName
---

# IFaxJob::get_UserName


## -description

The <b>IFaxJob::get_UserName</b> property is a null-terminated string that contains the name of the user who submitted the fax job to the job queue. The <b>IFaxJob::get_UserName</b> property applies only to outgoing fax transmissions.


This property is read-only.

## -parameters

## -remarks

You can use the <b>IFaxJob::get_UserName</b> property to retrieve the name of the person who initiated the fax job.

<b>IFaxJob::get_UserName</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjob">IFaxJob</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxjob-get-sendername-vb">IFaxJob::get_SenderName</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjobs">IFaxJobs</a>