---
UID: NF:faxcomex.IFaxOutgoingQueue.get_UseDeviceTSID
title: IFaxOutgoingQueue::get_UseDeviceTSID
author: windows-sdk-content
description: The IFaxOutgoingQueue::get_UseDeviceTSID property is a Boolean value that indicates whether the fax service uses the device transmitting station identifier (TSID) instead of a sender TSID.
old-location: fax\_mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_usedevicetsid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_72uc.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxOutgoingQueue interface [Fax Service],UseDeviceTSID property, IFaxOutgoingQueue.UseDeviceTSID, IFaxOutgoingQueue.get_UseDeviceTSID, IFaxOutgoingQueue.put_UseDeviceTSID, IFaxOutgoingQueue::UseDeviceTSID, IFaxOutgoingQueue::get_UseDeviceTSID, IFaxOutgoingQueue::put_UseDeviceTSID, UseDeviceTSID property [Fax Service], UseDeviceTSID property [Fax Service],IFaxOutgoingQueue interface, _mfax_faxoutgoingqueue.usedevicetsid, fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_usedevicetsid_cpp, fax._mfax_faxoutgoingqueue_usedevicetsid, faxcomex/IFaxOutgoingQueue::UseDeviceTSID, faxcomex/IFaxOutgoingQueue::get_UseDeviceTSID, faxcomex/IFaxOutgoingQueue::put_UseDeviceTSID, get_UseDeviceTSID
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
 - IFaxOutgoingQueue.UseDeviceTSID
 - IFaxOutgoingQueue.get_UseDeviceTSID
 - IFaxOutgoingQueue.put_UseDeviceTSID
 - IFaxOutgoingQueue.get_UseDeviceTSID
 - IFaxOutgoingQueue.put_UseDeviceTSID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingQueue::get_UseDeviceTSID


## -description


The <b>IFaxOutgoingQueue::get_UseDeviceTSID</b> property is a Boolean value that indicates whether the fax service uses the device transmitting station identifier (TSID) instead of a sender TSID. 

This property is read/write.


## -parameters


## -remarks



If this property is equal to <b>TRUE</b>, the fax service uses the device TSID rather than a user-specified TSID. If this property is equal to <b>FALSE</b>, the fax service uses a user-specified TSID.

To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/bad77c9e-2ae5-41a6-ace3-b4b92eb66cc2">FaxOutgoingQueue</a>



<a href="https://msdn.microsoft.com/2a6fede7-3fb8-495a-a8b1-81b53a701a16">IFaxOutgoingQueue</a>



<a href="https://msdn.microsoft.com/64866029-686e-451b-b7b5-33b5235ad307">Setting the Outgoing Queue Properties</a>
 

 

