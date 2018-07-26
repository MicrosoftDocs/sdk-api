---
UID: NF:faxcom.IFaxJob.get_DiscountSend
title: IFaxJob::get_DiscountSend
author: windows-sdk-content
description: The DiscountSend property is a Boolean value that indicates whether the fax server will transmit the fax job during the discount rate period. The discount period applies only to outgoing fax transmissions.
old-location: fax\_mfax_ifaxjob_get_discountsend_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8h9g.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: DiscountSend property [Fax Service], DiscountSend property [Fax Service],FaxJob object, FaxJob object [Fax Service],DiscountSend property, FaxJob.DiscountSend, IFaxJob.get_DiscountSend, IFaxJob::get_DiscountSend, _mfax_ifaxjob_get_discountsend, fax._mfax_ifaxjob_get_discountsend, fax._mfax_ifaxjob_get_discountsend_vb, get_DiscountSend
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ShellWindowTypeConstants
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - FaxJob.DiscountSend
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
<a href="https://msdn.microsoft.com/library/ms691308(v=VS.85).aspx">DiscountRateStartMinute</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/ms690899(v=VS.85).aspx">DiscountRateEndMinute</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/ms690858(v=VS.85).aspx">DiscountRateStartHour</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/ms691317(v=VS.85).aspx">DiscountRateEndHour</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690298(v=VS.85).aspx">FaxJob</a>



<a href="https://msdn.microsoft.com/library/ms692310(v=VS.85).aspx">IFaxJob</a>



<a href="https://msdn.microsoft.com/library/ms692372(v=VS.85).aspx">IFaxJobs</a>



<a href="https://msdn.microsoft.com/library/ms691821(v=VS.85).aspx">Managing Fax Jobs</a>
 

 

