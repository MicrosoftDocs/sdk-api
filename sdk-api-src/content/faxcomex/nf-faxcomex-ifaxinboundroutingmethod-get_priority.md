---
UID: NF:faxcomex.IFaxInboundRoutingMethod.get_Priority
title: IFaxInboundRoutingMethod::get_Priority
author: windows-sdk-content
description: The Priority property is a value associated with the order in which the fax service calls the routing method when the service receives a fax job.
old-location: fax\_mfax_faxinboundroutingmethod_priority_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_4kqh_cpp.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFaxInboundRoutingMethod interface [Fax Service],Priority property, IFaxInboundRoutingMethod.Priority, IFaxInboundRoutingMethod.get_Priority, IFaxInboundRoutingMethod::Priority, IFaxInboundRoutingMethod::get_Priority, IFaxInboundRoutingMethod::put_Priority, Priority property [Fax Service], Priority property [Fax Service],IFaxInboundRoutingMethod interface, _mfax_faxinboundroutingmethod.priority_cpp, fax._mfax_faxinboundroutingmethod_priority_cpp, faxcomex/IFaxInboundRoutingMethod::Priority, faxcomex/IFaxInboundRoutingMethod::get_Priority, faxcomex/IFaxInboundRoutingMethod::put_Priority, get_Priority
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
 - IFaxInboundRoutingMethod.Priority
 - IFaxInboundRoutingMethod.get_Priority
 - IFaxInboundRoutingMethod.put_Priority
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxInboundRoutingMethod::get_Priority


## -description


The <a href="https://msdn.microsoft.com/23208ac4-68c8-4f62-b588-2d0a5575f87c">Priority</a> property is a value associated with the order in which the fax service calls the routing method when the service receives a fax job.

This property is read/write.


## -parameters


## -remarks



Valid values for this property are 1 through <i>n</i>, where 1 is the highest priority.

You should assign a unique priority value to each routing method. After you call the <a href="https://msdn.microsoft.com/7fd645f1-9162-46ea-89a9-0888d86ec187">IFaxInboundRoutingMethod::Save</a> method, the fax service sorts the routing methods by priority. If two routing methods have the same priority, the fax service will choose which will have a higher priority.

If you want a particular routing method to have the lowest possible priority, specify a very large value, such as 999999, and then call the <a href="https://msdn.microsoft.com/7fd645f1-9162-46ea-89a9-0888d86ec187">IFaxInboundRoutingMethod::Save</a> method.

To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/8eb68201-4c87-41ce-a401-a039b5ad454d">FaxInboundRoutingMethod</a>



<a href="https://msdn.microsoft.com/ca33c439-24e7-4b85-8e29-a0a0176f0ae2">IFaxInboundRoutingMethod</a>



<a href="https://msdn.microsoft.com/cef24608-cab1-4090-aa94-3a1b76733e98">Visual Basic Example</a>
 

 

