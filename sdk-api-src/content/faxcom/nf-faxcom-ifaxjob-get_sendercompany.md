---
UID: NF:faxcom.IFaxJob.get_SenderCompany
title: IFaxJob::get_SenderCompany
author: windows-sdk-content
description: The IFaxJob::get_SenderCompany property is a null-terminated string that contains the company name for the sender of the fax job. The IFaxJob::get_SenderCompany property applies only to outgoing fax transmissions.
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_sendercompany_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7uk9.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IFaxJob interface [Fax Service],SenderCompany property, IFaxJob.SenderCompany, IFaxJob.get_SenderCompany, IFaxJob::SenderCompany, IFaxJob::get_SenderCompany, SenderCompany property [Fax Service], SenderCompany property [Fax Service],IFaxJob interface, _mfax_ifaxjob_get_sendercompany, fax._mfax_ifaxjob_get_sendercompany, fax._mfax_ifaxjob_mfax_ifaxjob_get_sendercompany_cpp, faxcom/IFaxJob::SenderCompany, faxcom/IFaxJob::get_SenderCompany, get_SenderCompany
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
 - IFaxJob.SenderCompany
 - IFaxJob.get_SenderCompany
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxJob::get_SenderCompany


## -description


The <b>IFaxJob::get_SenderCompany</b> property is a null-terminated string that contains the company name for the sender of the fax job. The <b>IFaxJob::get_SenderCompany</b> property applies only to outgoing fax transmissions.


This property is read-only.


## -parameters


## -remarks



If the sender's company is not available, the <b>IFaxJob::get_SenderCompany</b> property contains an empty string.

<b>IFaxJob::get_SenderCompany</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692310(v=VS.85).aspx">IFaxJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692372(v=VS.85).aspx">IFaxJobs</a>
 

 

