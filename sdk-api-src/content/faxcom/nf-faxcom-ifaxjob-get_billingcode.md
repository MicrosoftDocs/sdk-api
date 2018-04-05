---
UID: NF:faxcom.IFaxJob.get_BillingCode
title: IFaxJob::get_BillingCode method
author: windows-driver-content
description: The BillingCode property is a null-terminated string that contains an optional billing code that applies to the fax job.
old-location: fax\_mfax_ifaxjob_get_billingcode_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_2ov9.htm
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: BillingCode property [Fax Service], BillingCode property [Fax Service], FaxJob object, FaxJob object [Fax Service], BillingCode property, IFaxJob, IFaxJob::get_BillingCode, _mfax_ifaxjob_get_billingcode, fax._mfax_ifaxjob_get_billingcode, fax._mfax_ifaxjob_get_billingcode_vb, get_BillingCode,IFaxJob.get_BillingCode
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
req.typenames: ShellWindowTypeConstants
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Faxcom.dll
api_name:
-	FaxJob.BillingCode
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxJob::get_BillingCode method


## -description


The <b>BillingCode</b> property is a null-terminated string that contains an optional billing code that applies to the fax job.

This property is read-only.


## -parameters


## -remarks



If billing information is not available, the <b>BillingCode</b> property contains an empty string.

<b>BillingCode</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.






## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/c6e95bae-c1f8-4636-9847-7c66187cfc8d">FaxJob</a>



<a href="https://msdn.microsoft.com/48de5e31-0286-4b7a-a86b-46411bf0e9e8">IFaxJob</a>



<a href="https://msdn.microsoft.com/c9e548c4-9381-4b7d-9a9d-55fbc59f198f">IFaxJobs</a>
 

 

