---
UID: NF:faxcom.IFaxPort.get_Priority
title: IFaxPort::get_Priority
author: windows-driver-content
description: The Priority property is a number representing the transmission priority designated for a specified fax port. Priority determines the relative order in which available fax devices send outgoing transmissions.
old-location: fax\_mfax_ifaxport_get_priority_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0515.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: FaxPort object [Fax Service],Priority property, FaxPort.Priority, IFaxPort.get_Priority, IFaxPort::get_Priority, Priority property [Fax Service], Priority property [Fax Service],FaxPort object, _mfax_ifaxport_get_priority, fax._mfax_ifaxport_get_priority, fax._mfax_ifaxport_get_priority_vb, get_Priority
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
-	FaxPort.Priority
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxPort::get_Priority


## -description


The <b>Priority</b> property is a number representing the transmission priority designated for a specified fax port. Priority determines the relative order in which available fax devices send outgoing transmissions.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  Before setting a value for this property, a fax client application can call the <a href="https://msdn.microsoft.com/c88c2855-51cd-404e-a89f-cc42f456f51c">CanModify</a> property to ensure that the client has permission to modify configuration information for the specified fax port.</div>
<div> </div>
When the fax server initiates an outgoing fax transmission, it chooses the fax port with the highest priority and send capability. If that port is not available, the server selects the next available port that follows in rank order, and so on. When a client application changes the priority for a fax port, the fax service adjusts the priority for the other fax ports attached to the server. The <b>Priority</b> property has no effect on incoming transmissions.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/7888d042-7d85-4921-b233-f6e95e0c80d9">FaxPort</a>



<a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a>



<a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a>
 

 

