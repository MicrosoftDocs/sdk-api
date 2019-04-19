---
UID: NF:faxcomex.IFaxIncomingMessage.get_DeviceName
title: IFaxIncomingMessage::get_DeviceName (faxcomex.h)
author: windows-sdk-content
description: The DeviceName property is a null-terminated string that contains the name of the device on which the inbound fax message was received.
old-location: fax\_mfax_faxincomingmessage_cpp_mfax_faxincomingmessage_devicename_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5fhh.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DeviceName property [Fax Service], DeviceName property [Fax Service],IFaxIncomingMessage interface, IFaxIncomingMessage interface [Fax Service],DeviceName property, IFaxIncomingMessage.DeviceName, IFaxIncomingMessage.get_DeviceName, IFaxIncomingMessage::DeviceName, IFaxIncomingMessage::get_DeviceName, _mfax_faxincomingmessage.devicename, fax._mfax_faxincomingmessage_cpp_mfax_faxincomingmessage_devicename_cpp, fax._mfax_faxincomingmessage_devicename, faxcomex/IFaxIncomingMessage::DeviceName, faxcomex/IFaxIncomingMessage::get_DeviceName, get_DeviceName
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
 - IFaxIncomingMessage.DeviceName
 - IFaxIncomingMessage.get_DeviceName
 - IFaxIncomingMessage.get_DeviceName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxIncomingMessage::get_DeviceName


## -description


The <b>DeviceName</b> property is a null-terminated string that contains the name of the device on which the inbound fax message was received.

This property is read-only.


## -parameters


## -remarks



This method returns the name of the fax device rather than the device ID. This is useful because an administrator may remove the device ID after completion of the fax job and before the client's query of the archive of inbound fax messages.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686126(v=VS.85).aspx">FaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms686128(v=VS.85).aspx">IFaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693406(v=VS.85).aspx">Visual Basic Example</a>
 

 

