---
UID: NF:faxcomex.IFaxOutgoingMessage.get_DeviceName
title: IFaxOutgoingMessage::get_DeviceName
author: windows-sdk-content
description: The IFaxOutgoingMessage::get_DeviceName property is a null-terminated string that contains the name of the device on which the fax message was transmitted.
old-location: fax\_mfax_faxoutgoingmessage_cpp_mfax_faxoutgoingmessage_devicename_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_0qw5.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DeviceName property [Fax Service], DeviceName property [Fax Service],IFaxOutgoingMessage interface, IFaxOutgoingMessage interface [Fax Service],DeviceName property, IFaxOutgoingMessage.DeviceName, IFaxOutgoingMessage.get_DeviceName, IFaxOutgoingMessage::DeviceName, IFaxOutgoingMessage::get_DeviceName, _mfax_faxoutgoingmessage.devicename, fax._mfax_faxoutgoingmessage_cpp_mfax_faxoutgoingmessage_devicename_cpp, fax._mfax_faxoutgoingmessage_devicename, faxcomex/IFaxOutgoingMessage::DeviceName, faxcomex/IFaxOutgoingMessage::get_DeviceName, get_DeviceName
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
 - IFaxOutgoingMessage.DeviceName
 - IFaxOutgoingMessage.get_DeviceName
 - IFaxOutgoingMessage.get_DeviceName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingMessage::get_DeviceName


## -description


The <b>IFaxOutgoingMessage::get_DeviceName</b> property is a null-terminated string that contains the name of the device on which the fax message was transmitted.

This property is read-only.


## -parameters


## -remarks



This method returns the name of the fax device rather than the device ID. This is useful because an administrator may remove the device ID after completion of the fax job and before the client's query of the archive of fax messages.




## -see-also




<a href="https://msdn.microsoft.com/fb06254f-f37b-4783-b4fd-42b5c5a28496">FaxOutgoingMessage</a>



<a href="https://msdn.microsoft.com/7423ccd1-5eb6-402f-99fb-2cbed386450a">IFaxOutgoingMessage</a>



<a href="https://msdn.microsoft.com/072eb2cc-7fd9-4f8e-8583-44384357e708">Visual Basic Example</a>
 

 

