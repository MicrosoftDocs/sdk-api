---
UID: NF:mbnapi.IMbnSmsReadMsgPdu.get_Message
title: IMbnSmsReadMsgPdu::get_Message (mbnapi.h)
description: Message in WMT format as used by CDMA devices.
old-location: mbn\imbnsmsreadmsgpdu_message.htm
tech.root: mbn
ms.assetid: 83135a78-096c-4690-be07-a64febecd66c
ms.date: 12/05/2018
ms.keywords: IMbnSmsReadMsgPdu interface [Microsoft Broadband Networks],Message property, IMbnSmsReadMsgPdu.Message, IMbnSmsReadMsgPdu.get_Message, IMbnSmsReadMsgPdu::Message, IMbnSmsReadMsgPdu::get_Message, Message property [Microsoft Broadband Networks], Message property [Microsoft Broadband Networks],IMbnSmsReadMsgPdu interface, get_Message, mbn.imbnsmsreadmsgpdu_message, mbnapi/IMbnSmsReadMsgPdu::Message, mbnapi/IMbnSmsReadMsgPdu::get_Message
f1_keywords:
- mbnapi/IMbnSmsReadMsgPdu.Message
dev_langs:
- c++
req.header: mbnapi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnSmsReadMsgPdu::get_Message


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The message in WMT format  as used by CDMA devices.

This property is read-only.


## -parameters


## -remarks



For CDMA devices, this returns a byte array representing a message as defined in section 3.4.2.1 SMS Point-to-Point Messageâ€ in the 3GPP2 specification C.S0015-A â€œShort Message Service (SMS) for Wideband Spread Spectrum Systemsâ€. SMS will only support the Wireless Messaging Teleservice (WMT) format.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsreadmsgpdu">IMbnSmsReadMsgPdu</a>
 

 

