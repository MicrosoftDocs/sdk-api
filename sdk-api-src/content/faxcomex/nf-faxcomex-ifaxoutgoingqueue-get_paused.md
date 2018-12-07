---
UID: NF:faxcomex.IFaxOutgoingQueue.get_Paused
title: IFaxOutgoingQueue::get_Paused
author: windows-sdk-content
description: The IFaxOutgoingQueue::get_Paused property is a Boolean value that indicates whether the job queue for outgoing faxes is paused.
old-location: fax\_mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_paused_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_81b8.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxOutgoingQueue interface [Fax Service],Paused property, IFaxOutgoingQueue.Paused, IFaxOutgoingQueue.get_Paused, IFaxOutgoingQueue.put_Paused, IFaxOutgoingQueue::Paused, IFaxOutgoingQueue::get_Paused, IFaxOutgoingQueue::put_Paused, Paused property [Fax Service], Paused property [Fax Service],IFaxOutgoingQueue interface, _mfax_faxoutgoingqueue.paused, fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_paused_cpp, fax._mfax_faxoutgoingqueue_paused, faxcomex/IFaxOutgoingQueue::Paused, faxcomex/IFaxOutgoingQueue::get_Paused, faxcomex/IFaxOutgoingQueue::put_Paused, get_Paused
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxOutgoingQueue.Paused
 - IFaxOutgoingQueue.get_Paused
 - IFaxOutgoingQueue.put_Paused
 - IFaxOutgoingQueue.get_Paused
 - IFaxOutgoingQueue.put_Paused
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingQueue::get_Paused


## -description


The <b>IFaxOutgoingQueue::get_Paused</b> property is a Boolean value that indicates whether the job queue for outgoing faxes is paused. 

This property is read/write.


## -parameters


## -remarks



If this property is equal to <b>TRUE</b>, the job queue is paused and the fax service is not processing jobs in the queue. If this property is equal to <b>FALSE</b>, the outgoing queue is not paused.

To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/bad77c9e-2ae5-41a6-ace3-b4b92eb66cc2">FaxOutgoingQueue</a>



<a href="https://msdn.microsoft.com/2a6fede7-3fb8-495a-a8b1-81b53a701a16">IFaxOutgoingQueue</a>



<a href="https://msdn.microsoft.com/64866029-686e-451b-b7b5-33b5235ad307">Setting the Outgoing Queue Properties</a>
 

 

