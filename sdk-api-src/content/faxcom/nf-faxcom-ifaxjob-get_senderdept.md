---
UID: NF:faxcom.IFaxJob.get_SenderDept
title: IFaxJob::get_SenderDept
author: windows-sdk-content
description: The IFaxJob::get_SenderDept property is a null-terminated string that contains the department identifier for the sender of the fax job. The IFaxJob::get_SenderDept property applies only to outgoing fax transmissions.
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_senderdept_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_71mc.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxJob interface [Fax Service],SenderDept property, IFaxJob.SenderDept, IFaxJob.get_SenderDept, IFaxJob::SenderDept, IFaxJob::get_SenderDept, SenderDept property [Fax Service], SenderDept property [Fax Service],IFaxJob interface, _mfax_ifaxjob_get_senderdept, fax._mfax_ifaxjob_get_senderdept, fax._mfax_ifaxjob_mfax_ifaxjob_get_senderdept_cpp, faxcom/IFaxJob::SenderDept, faxcom/IFaxJob::get_SenderDept, get_SenderDept
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
 - IFaxJob.SenderDept
 - IFaxJob.get_SenderDept
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxJob::get_SenderDept


## -description


The <b>IFaxJob::get_SenderDept</b> property is a null-terminated string that contains the department identifier for the sender of the fax job. The <b>IFaxJob::get_SenderDept</b> property applies only to outgoing fax transmissions.

This property is read-only.


## -parameters


## -remarks



If the sender's department is not available, the <b>IFaxJob::get_SenderDept</b> property contains an empty string.

The <b>IFaxJob::get_SenderDept</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692310(v=VS.85).aspx">IFaxJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692372(v=VS.85).aspx">IFaxJobs</a>
 

 

