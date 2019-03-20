---
UID: NF:faxcom.IFaxJob.get_RecipientName
title: IFaxJob::get_RecipientName (faxcom.h)
author: windows-sdk-content
description: The IFaxJob::get_RecipientName property is a null-terminated string that contains the name of the recipient of the fax job.
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_recipientname_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5vvp.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxJob interface [Fax Service],RecipientName property, IFaxJob.RecipientName, IFaxJob.get_RecipientName, IFaxJob::RecipientName, IFaxJob::get_RecipientName, RecipientName property [Fax Service], RecipientName property [Fax Service],IFaxJob interface, _mfax_ifaxjob_get_recipientname, fax._mfax_ifaxjob_get_recipientname, fax._mfax_ifaxjob_mfax_ifaxjob_get_recipientname_cpp, faxcom/IFaxJob::RecipientName, faxcom/IFaxJob::get_RecipientName, get_RecipientName
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
 - IFaxJob.RecipientName
 - IFaxJob.get_RecipientName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxJob::get_RecipientName


## -description


The <b>IFaxJob::get_RecipientName</b> property is a null-terminated string that contains the name of the recipient of the fax job.

This property is read-only.


## -parameters


## -remarks



If the recipient's name is not available, the <b>IFaxJob::get_RecipientName</b> property contains an empty string.

<b>IFaxJob::get_RecipientName</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.






## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692310(v=VS.85).aspx">IFaxJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692372(v=VS.85).aspx">IFaxJobs</a>
 

 

