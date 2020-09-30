---
UID: NF:faxcomex.IFaxOutgoingMessage.get_DeviceName
title: IFaxOutgoingMessage::get_DeviceName (faxcomex.h)
description: The IFaxOutgoingMessage::get_DeviceName property is a null-terminated string that contains the name of the device on which the fax message was transmitted.
helpviewer_keywords: ["DeviceName property [Fax Service]","DeviceName property [Fax Service]","IFaxOutgoingMessage interface","IFaxOutgoingMessage interface [Fax Service]","DeviceName property","IFaxOutgoingMessage.DeviceName","IFaxOutgoingMessage.get_DeviceName","IFaxOutgoingMessage::DeviceName","IFaxOutgoingMessage::get_DeviceName","_mfax_faxoutgoingmessage.devicename","fax._mfax_faxoutgoingmessage_cpp_mfax_faxoutgoingmessage_devicename_cpp","fax._mfax_faxoutgoingmessage_devicename","faxcomex/IFaxOutgoingMessage::DeviceName","faxcomex/IFaxOutgoingMessage::get_DeviceName","get_DeviceName"]
old-location: fax\_mfax_faxoutgoingmessage_cpp_mfax_faxoutgoingmessage_devicename_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_0qw5.htm
ms.date: 12/05/2018
ms.keywords: DeviceName property [Fax Service], DeviceName property [Fax Service],IFaxOutgoingMessage interface, IFaxOutgoingMessage interface [Fax Service],DeviceName property, IFaxOutgoingMessage.DeviceName, IFaxOutgoingMessage.get_DeviceName, IFaxOutgoingMessage::DeviceName, IFaxOutgoingMessage::get_DeviceName, _mfax_faxoutgoingmessage.devicename, fax._mfax_faxoutgoingmessage_cpp_mfax_faxoutgoingmessage_devicename_cpp, fax._mfax_faxoutgoingmessage_devicename, faxcomex/IFaxOutgoingMessage::DeviceName, faxcomex/IFaxOutgoingMessage::get_DeviceName, get_DeviceName
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxOutgoingMessage::get_DeviceName
 - faxcomex/IFaxOutgoingMessage::get_DeviceName
dev_langs:
 - c++
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
---

# IFaxOutgoingMessage::get_DeviceName


## -description

The <b>IFaxOutgoingMessage::get_DeviceName</b> property is a null-terminated string that contains the name of the device on which the fax message was transmitted.

This property is read-only.

## -parameters

## -remarks

This method returns the name of the fax device rather than the device ID. This is useful because an administrator may remove the device ID after completion of the fax job and before the client's query of the archive of fax messages.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage">FaxOutgoingMessage</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessage">IFaxOutgoingMessage</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-opening-a-fax-from-the-outgoing-archive">Visual Basic Example</a>