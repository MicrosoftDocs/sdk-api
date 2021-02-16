---
UID: NF:faxcom.IFaxJob.get_DisplayName
title: IFaxJob::get_DisplayName (faxcom.h)
description: The IFaxJob::get_DisplayName property is a null-terminated string that contains the user-friendly name to associate with the fax job.
helpviewer_keywords: ["DisplayName property [Fax Service]","DisplayName property [Fax Service]","IFaxJob interface","IFaxJob interface [Fax Service]","DisplayName property","IFaxJob.DisplayName","IFaxJob.get_DisplayName","IFaxJob::DisplayName","IFaxJob::get_DisplayName","_mfax_ifaxjob_get_displayname","fax._mfax_ifaxjob_get_displayname","fax._mfax_ifaxjob_mfax_ifaxjob_get_displayname_cpp","faxcom/IFaxJob::DisplayName","faxcom/IFaxJob::get_DisplayName","get_DisplayName"]
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_displayname_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8b39.htm
ms.date: 12/05/2018
ms.keywords: DisplayName property [Fax Service], DisplayName property [Fax Service],IFaxJob interface, IFaxJob interface [Fax Service],DisplayName property, IFaxJob.DisplayName, IFaxJob.get_DisplayName, IFaxJob::DisplayName, IFaxJob::get_DisplayName, _mfax_ifaxjob_get_displayname, fax._mfax_ifaxjob_get_displayname, fax._mfax_ifaxjob_mfax_ifaxjob_get_displayname_cpp, faxcom/IFaxJob::DisplayName, faxcom/IFaxJob::get_DisplayName, get_DisplayName
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
 - IFaxJob::get_DisplayName
 - faxcom/IFaxJob::get_DisplayName
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
 - IFaxJob.DisplayName
 - IFaxJob.get_DisplayName
---

# IFaxJob::get_DisplayName


## -description

The <b>IFaxJob::get_DisplayName</b> property is a null-terminated string that contains the user-friendly name to associate with the fax job.


This property is read-only.

## -parameters

## -remarks

You can use the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxjob-get-jobid-vb">IFaxJob::get_JobId</a> property to uniquely identify a fax job because it is possible for multiple fax jobs to have the same <b>IFaxJob::get_DisplayName</b> property.

<b>IFaxJob::get_DisplayName</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjob">IFaxJob</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxjob-get-jobid-vb">IFaxJob::get_JobId</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjobs">IFaxJobs</a>