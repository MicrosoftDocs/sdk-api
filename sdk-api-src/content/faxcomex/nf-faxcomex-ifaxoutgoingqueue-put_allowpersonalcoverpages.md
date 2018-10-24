---
UID: NF:faxcomex.IFaxOutgoingQueue.put_AllowPersonalCoverPages
title: IFaxOutgoingQueue::put_AllowPersonalCoverPages
author: windows-sdk-content
description: The AllowPersonalCoverPages property is a Boolean value that indicates whether fax client applications can include a user-designed cover page with fax transmissions.
old-location: fax\_mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_allowpersonalcoverpages_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_5cc3.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: AllowPersonalCoverPages property [Fax Service], AllowPersonalCoverPages property [Fax Service],IFaxOutgoingQueue interface, IFaxOutgoingQueue interface [Fax Service],AllowPersonalCoverPages property, IFaxOutgoingQueue.AllowPersonalCoverPages, IFaxOutgoingQueue.put_AllowPersonalCoverPages, IFaxOutgoingQueue::AllowPersonalCoverPages, IFaxOutgoingQueue::get_AllowPersonalCoverPages, IFaxOutgoingQueue::put_AllowPersonalCoverPages, _mfax_faxoutgoingqueue.allowpersonalcoverpages, fax._mfax_faxoutgoingqueue_allowpersonalcoverpages, fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_allowpersonalcoverpages_cpp, faxcomex/IFaxOutgoingQueue::AllowPersonalCoverPages, faxcomex/IFaxOutgoingQueue::get_AllowPersonalCoverPages, faxcomex/IFaxOutgoingQueue::put_AllowPersonalCoverPages, put_AllowPersonalCoverPages
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
 - IFaxOutgoingQueue.AllowPersonalCoverPages
 - IFaxOutgoingQueue.get_AllowPersonalCoverPages
 - IFaxOutgoingQueue.put_AllowPersonalCoverPages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingQueue::put_AllowPersonalCoverPages


## -description


The AllowPersonalCoverPages property is a Boolean value that indicates whether fax client applications can include a user-designed cover page with fax transmissions.

This property is read/write.


## -parameters


## -remarks



If this property is equal to <b>TRUE</b>, clients can include personal cover page files with fax transmissions. If this property is equal to <b>FALSE</b>, clients must use a common cover page file stored on the fax server. 

To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/bad77c9e-2ae5-41a6-ace3-b4b92eb66cc2">FaxOutgoingQueue</a>



<a href="https://msdn.microsoft.com/2a6fede7-3fb8-495a-a8b1-81b53a701a16">IFaxOutgoingQueue</a>



<a href="https://msdn.microsoft.com/64866029-686e-451b-b7b5-33b5235ad307">Setting the Outgoing Queue Properties</a>
 

 

