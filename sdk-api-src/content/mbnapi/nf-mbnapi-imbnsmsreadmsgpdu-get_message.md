---
UID: NF:mbnapi.IMbnSmsReadMsgPdu.get_Message
title: IMbnSmsReadMsgPdu::get_Message
author: windows-sdk-content
description: Message in WMT format as used by CDMA devices.
old-location: mbn\imbnsmsreadmsgpdu_message.htm
old-project: mbn
ms.assetid: 83135a78-096c-4690-be07-a64febecd66c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IMbnSmsReadMsgPdu interface [Microsoft Broadband Networks],Message property, IMbnSmsReadMsgPdu.Message, IMbnSmsReadMsgPdu.get_Message, IMbnSmsReadMsgPdu::Message, IMbnSmsReadMsgPdu::get_Message, Message property [Microsoft Broadband Networks], Message property [Microsoft Broadband Networks],IMbnSmsReadMsgPdu interface, get_Message, mbn.imbnsmsreadmsgpdu_message, mbnapi/IMbnSmsReadMsgPdu::Message, mbnapi/IMbnSmsReadMsgPdu::get_Message
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnSmsReadMsgPdu.Message
 - IMbnSmsReadMsgPdu.get_Message
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnSmsReadMsgPdu::get_Message


## -description


The message in WMT format  as used by CDMA devices.

This property is read-only.


## -parameters


## -remarks



For CDMA devices, this returns a byte array representing a message as defined in section 3.4.2.1 SMS Point-to-Point Messageâ€ in the 3GPP2 specification C.S0015-A â€œShort Message Service (SMS) for Wideband Spread Spectrum Systemsâ€. SMS will only support the Wireless Messaging Teleservice (WMT) format.




## -see-also




<a href="https://msdn.microsoft.com/dc0e15c4-6203-4105-9d19-5931b27047d2">IMbnSmsReadMsgPdu</a>
 

 

