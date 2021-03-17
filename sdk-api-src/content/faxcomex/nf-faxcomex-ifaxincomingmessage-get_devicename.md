---
UID: NF:faxcomex.IFaxIncomingMessage.get_DeviceName
title: IFaxIncomingMessage::get_DeviceName (faxcomex.h)
description: The DeviceName property is a null-terminated string that contains the name of the device on which the inbound fax message was received.
helpviewer_keywords: ["DeviceName property [Fax Service]","DeviceName property [Fax Service]","IFaxIncomingMessage interface","IFaxIncomingMessage interface [Fax Service]","DeviceName property","IFaxIncomingMessage.DeviceName","IFaxIncomingMessage.get_DeviceName","IFaxIncomingMessage::DeviceName","IFaxIncomingMessage::get_DeviceName","_mfax_faxincomingmessage.devicename","fax._mfax_faxincomingmessage_cpp_mfax_faxincomingmessage_devicename_cpp","fax._mfax_faxincomingmessage_devicename","faxcomex/IFaxIncomingMessage::DeviceName","faxcomex/IFaxIncomingMessage::get_DeviceName","get_DeviceName"]
old-location: fax\_mfax_faxincomingmessage_cpp_mfax_faxincomingmessage_devicename_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5fhh.htm
ms.date: 12/05/2018
ms.keywords: DeviceName property [Fax Service], DeviceName property [Fax Service],IFaxIncomingMessage interface, IFaxIncomingMessage interface [Fax Service],DeviceName property, IFaxIncomingMessage.DeviceName, IFaxIncomingMessage.get_DeviceName, IFaxIncomingMessage::DeviceName, IFaxIncomingMessage::get_DeviceName, _mfax_faxincomingmessage.devicename, fax._mfax_faxincomingmessage_cpp_mfax_faxincomingmessage_devicename_cpp, fax._mfax_faxincomingmessage_devicename, faxcomex/IFaxIncomingMessage::DeviceName, faxcomex/IFaxIncomingMessage::get_DeviceName, get_DeviceName
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
 - IFaxIncomingMessage::get_DeviceName
 - faxcomex/IFaxIncomingMessage::get_DeviceName
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
 - IFaxIncomingMessage.DeviceName
 - IFaxIncomingMessage.get_DeviceName
 - IFaxIncomingMessage.get_DeviceName
---

# IFaxIncomingMessage::get_DeviceName


## -description

The <b>DeviceName</b> property is a null-terminated string that contains the name of the device on which the inbound fax message was received.

This property is read-only.

## -parameters

## -remarks

This method returns the name of the fax device rather than the device ID. This is useful because an administrator may remove the device ID after completion of the fax job and before the client's query of the archive of inbound fax messages.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage">FaxIncomingMessage</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessage">IFaxIncomingMessage</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-the-incoming-archive">Visual Basic Example</a>