---
UID: NF:faxcomex.IFaxIncomingMessage2.get_SenderFaxNumber
title: IFaxIncomingMessage2::get_SenderFaxNumber
author: windows-sdk-content
description: Contains the sender's fax number associated with the inbound fax message. This property is a null-terminated string.
old-location: fax\_mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_senderfaxnumber_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxincomingmessage2\senderfaxnumber.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxIncomingMessage2 interface [Fax Service],SenderFaxNumber property, IFaxIncomingMessage2.SenderFaxNumber, IFaxIncomingMessage2.get_SenderFaxNumber, IFaxIncomingMessage2.put_SenderFaxNumber, IFaxIncomingMessage2::SenderFaxNumber, IFaxIncomingMessage2::get_SenderFaxNumber, IFaxIncomingMessage2::put_SenderFaxNumber, SenderFaxNumber property [Fax Service], SenderFaxNumber property [Fax Service],IFaxIncomingMessage2 interface, _mfax_faxincomingmessage.senderfaxnumber, fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_senderfaxnumber_cpp, fax._mfax_faxincomingmessage_senderfaxnumber, faxcomex/IFaxIncomingMessage2::SenderFaxNumber, faxcomex/IFaxIncomingMessage2::get_SenderFaxNumber, faxcomex/IFaxIncomingMessage2::put_SenderFaxNumber, get_SenderFaxNumber
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IFaxIncomingMessage2.SenderFaxNumber
 - IFaxIncomingMessage2.get_SenderFaxNumber
 - IFaxIncomingMessage2.put_SenderFaxNumber
 - IFaxIncomingMessage2.get_SenderFaxNumber
 - IFaxIncomingMessage2.put_SenderFaxNumber
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingMessage2::get_SenderFaxNumber


## -description


Contains the sender's fax number associated with the inbound fax message. This property is a null-terminated string. 


<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div><div> </div>This property is read/write.


## -parameters


## -remarks



A received message starts with a null value for the sender's fax number when it arrives. A <a href="https://msdn.microsoft.com/ede1c31f-e53a-4ddc-ba25-6fcadadd513a">routing assistant</a> can specify the sender's fax number when the fax is reassigned.




## -see-also




<a href="https://msdn.microsoft.com/ee546d4c-e580-4738-a5d2-0b10c5d8a1ab">FaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/b3dc429e-1470-4e7d-8cd5-9cadb0052051">IFaxIncomingMessage2</a>
 

 

