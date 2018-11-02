---
UID: NF:faxcom.IFaxJob.get_BillingCode
title: IFaxJob::get_BillingCode
author: windows-sdk-content
description: The IFaxJob::get_BillingCode property is a null-terminated string that contains an optional billing code that applies to the fax job.
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_billingcode_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_2ov9.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: BillingCode property [Fax Service], BillingCode property [Fax Service],IFaxJob interface, IFaxJob interface [Fax Service],BillingCode property, IFaxJob.BillingCode, IFaxJob.get_BillingCode, IFaxJob::BillingCode, IFaxJob::get_BillingCode, _mfax_ifaxjob_get_billingcode, fax._mfax_ifaxjob_get_billingcode, fax._mfax_ifaxjob_mfax_ifaxjob_get_billingcode_cpp, faxcom/IFaxJob::BillingCode, faxcom/IFaxJob::get_BillingCode, get_BillingCode
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
 - IFaxJob.BillingCode
 - IFaxJob.get_BillingCode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxJob::get_BillingCode


## -description


The <b>IFaxJob::get_BillingCode</b> property is a null-terminated string that contains an optional billing code that applies to the fax job.

This property is read-only.


## -parameters


## -remarks



If billing information is not available, the <b>IFaxJob::get_BillingCode</b> property contains an empty string.

<b>IFaxJob::get_BillingCode</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.






## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692310(v=VS.85).aspx">IFaxJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692372(v=VS.85).aspx">IFaxJobs</a>
 

 

