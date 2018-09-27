---
UID: NF:faxcom.IFaxJob.Refresh
title: IFaxJob::Refresh
author: windows-sdk-content
description: The IFaxJob::Refresh method updates FaxJob object information for the associated fax job.
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7bqg.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IFaxJob interface [Fax Service],Refresh method, IFaxJob.Refresh, IFaxJob::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxJob interface, _mfax_ifaxjob_refresh, fax._mfax_ifaxjob_mfax_ifaxjob_refresh_cpp, fax._mfax_ifaxjob_refresh, faxcom/IFaxJob::Refresh
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxJob::Refresh


## -description


The <b>IFaxJob::Refresh</b> method updates <a href="https://msdn.microsoft.com/4c8376a4-dded-489e-a361-ce6edd0e17af">FaxJob</a> object information for the associated fax job.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call the <b>IFaxJob::Refresh</b> method to poll the fax service for new information about a specified fax job. After you successfully call <b>IFaxJob::Refresh</b>, you must call the appropriate <a href="https://msdn.microsoft.com/48de5e31-0286-4b7a-a86b-46411bf0e9e8">IFaxJob</a> interface method to retrieve new attribute values that are valid.

It is recommended that you limit calls to this method because frequent calls to <b>IFaxJob::Refresh</b> can degrade system performance.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/48de5e31-0286-4b7a-a86b-46411bf0e9e8">IFaxJob</a>



<a href="https://msdn.microsoft.com/c9e548c4-9381-4b7d-9a9d-55fbc59f198f">IFaxJobs</a>
 

 

