---
UID: NF:faxcomex.IFaxOutgoingQueue.get_AgeLimit
title: IFaxOutgoingQueue::get_AgeLimit
author: windows-sdk-content
description: The AgeLimit property is a value that indicates the number of days that the fax service retains an unsent job in the fax job queue.
old-location: fax\_mfax_faxoutgoingqueue_agelimit_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7qyc.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: AgeLimit property [Fax Service], AgeLimit property [Fax Service],FaxOutgoingQueue object, FaxOutgoingQueue object [Fax Service],AgeLimit property, FaxOutgoingQueue.AgeLimit, IFaxOutgoingQueue.get_AgeLimit, IFaxOutgoingQueue::get_AgeLimit, _mfax_faxoutgoingqueue.agelimit, fax._mfax_faxoutgoingqueue_agelimit, fax._mfax_faxoutgoingqueue_agelimit_vb, get_AgeLimit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - FaxOutgoingQueue.AgeLimit
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutgoingQueue::get_AgeLimit


## -description


The <b>AgeLimit</b> property is a value that indicates the number of days that the fax service retains an unsent job in the fax job queue. 

This property is read/write.


## -parameters


## -remarks



If the fax job remains in the outbound job queue longer than the value specified, the fax service deletes the job. If the value of this property is zero, the fax service does not enforce an age limit.

To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/bad77c9e-2ae5-41a6-ace3-b4b92eb66cc2">FaxOutgoingQueue</a>



<a href="https://msdn.microsoft.com/2a6fede7-3fb8-495a-a8b1-81b53a701a16">IFaxOutgoingQueue</a>



<a href="https://msdn.microsoft.com/64866029-686e-451b-b7b5-33b5235ad307">Setting the Outgoing Queue Properties</a>
 

 

