---
UID: NF:faxcomex.IFaxIncomingMessage2.put_SenderName
title: IFaxIncomingMessage2::put_SenderName
author: windows-sdk-content
description: Contains the name of the sender that is associated with the inbound fax message. This property is a null-terminated string.
old-location: fax\_mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_sendername_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxincomingmessage2\sendername.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IFaxIncomingMessage2 interface [Fax Service],SenderName property, IFaxIncomingMessage2.SenderName, IFaxIncomingMessage2.get_SenderName, IFaxIncomingMessage2.put_SenderName, IFaxIncomingMessage2::SenderName, IFaxIncomingMessage2::get_SenderName, IFaxIncomingMessage2::put_SenderName, SenderName property [Fax Service], SenderName property [Fax Service],IFaxIncomingMessage2 interface, _mfax_faxincomingmessage.sendername, fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_sendername_cpp, fax._mfax_faxincomingmessage_sendername, faxcomex/IFaxIncomingMessage2::SenderName, faxcomex/IFaxIncomingMessage2::get_SenderName, faxcomex/IFaxIncomingMessage2::put_SenderName, put_SenderName
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
 - IFaxIncomingMessage2.SenderName
 - IFaxIncomingMessage2.get_SenderName
 - IFaxIncomingMessage2.put_SenderName
 - IFaxIncomingMessage2.get_SenderName
 - IFaxIncomingMessage2.put_SenderName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingMessage2::put_SenderName


## -description


Contains the name of the sender that is associated with the inbound fax message. This property is a null-terminated string.


<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div><div> </div>This property is read/write.


## -parameters


## -remarks



A received message starts with a null value for the sender when it arrives. A sender can be specified by a <a href="https://msdn.microsoft.com/ede1c31f-e53a-4ddc-ba25-6fcadadd513a">routing assistant</a>when it is re-assigned.




## -see-also




<a href="https://msdn.microsoft.com/ee546d4c-e580-4738-a5d2-0b10c5d8a1ab">FaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/b3dc429e-1470-4e7d-8cd5-9cadb0052051">IFaxIncomingMessage2</a>
 

 

