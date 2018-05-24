---
UID: NF:faxcom.IFaxJob.get_DiscountSend
title: IFaxJob::get_DiscountSend
author: windows-driver-content
description: The DiscountSend property is a Boolean value that indicates whether the fax server will transmit the fax job during the discount rate period. The discount period applies only to outgoing fax transmissions.
old-location: fax\_mfax_ifaxjob_get_discountsend_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8h9g.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: DiscountSend property [Fax Service], DiscountSend property [Fax Service],FaxJob object, FaxJob object [Fax Service],DiscountSend property, FaxJob.DiscountSend, IFaxJob.get_DiscountSend, IFaxJob::get_DiscountSend, _mfax_ifaxjob_get_discountsend, fax._mfax_ifaxjob_get_discountsend, fax._mfax_ifaxjob_get_discountsend_vb, get_DiscountSend
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
-	FaxJob.DiscountSend
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxJob::get_DiscountSend


## -description


The <b>DiscountSend</b> property is a Boolean value that indicates whether the fax server will transmit the fax job during the discount rate period. The discount period applies only to outgoing fax transmissions. 

This property is read-only.


## -parameters


## -remarks



To determine the period during which the discount rate applies, you can use the following IFaxServer properties. 

<ul>
<li>
<a href="https://msdn.microsoft.com/5159eb01-d464-4cc3-8617-e785c97ff6ff">DiscountRateStartMinute</a>
</li>
<li>
<a href="https://msdn.microsoft.com/db9e206b-d398-4924-93b9-c7628043dd23">DiscountRateEndMinute</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1ba6f885-08a2-4ee5-9120-c9da3e01c570">DiscountRateStartHour</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a953c003-3a0c-4d75-a86f-6397ce776c2f">DiscountRateEndHour</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/c6e95bae-c1f8-4636-9847-7c66187cfc8d">FaxJob</a>



<a href="https://msdn.microsoft.com/48de5e31-0286-4b7a-a86b-46411bf0e9e8">IFaxJob</a>



<a href="https://msdn.microsoft.com/c9e548c4-9381-4b7d-9a9d-55fbc59f198f">IFaxJobs</a>



<a href="https://msdn.microsoft.com/7eb47777-cf5c-463d-bf19-5884c6fed04f">Managing Fax Jobs</a>
 

 

