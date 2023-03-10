---
UID: NE:faxcomex.FAX_DEVICE_RECEIVE_MODE_ENUM
title: FAX_DEVICE_RECEIVE_MODE_ENUM (faxcomex.h)
description: The FAX_DEVICE_RECEIVE_MODE_ENUM enumeration defines the way a device answers an incoming call.
helpviewer_keywords: ["FAX_DEVICE_RECEIVE_MODE_ENUM","FAX_DEVICE_RECEIVE_MODE_ENUM enumeration [Fax Service]","_mfax_fax_device_receive_mode_enum","fax._mfax_fax_device_receive_mode_enum","faxcomex/FAX_DEVICE_RECEIVE_MODE_ENUM","faxcomex/fdrmAUTO_ANSWER","faxcomex/fdrmMANUAL_ANSWER","faxcomex/fdrmNO_ANSWER","fdrmAUTO_ANSWER","fdrmMANUAL_ANSWER","fdrmNO_ANSWER"]
old-location: fax\_mfax_fax_device_receive_mode_enum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6ib1.htm
ms.date: 12/05/2018
ms.keywords: FAX_DEVICE_RECEIVE_MODE_ENUM, FAX_DEVICE_RECEIVE_MODE_ENUM enumeration [Fax Service], _mfax_fax_device_receive_mode_enum, fax._mfax_fax_device_receive_mode_enum, faxcomex/FAX_DEVICE_RECEIVE_MODE_ENUM, faxcomex/fdrmAUTO_ANSWER, faxcomex/fdrmMANUAL_ANSWER, faxcomex/fdrmNO_ANSWER, fdrmAUTO_ANSWER, fdrmMANUAL_ANSWER, fdrmNO_ANSWER
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FAX_DEVICE_RECEIVE_MODE_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FAX_DEVICE_RECEIVE_MODE_ENUM
 - faxcomex/FAX_DEVICE_RECEIVE_MODE_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxComex.h
api_name:
 - FAX_DEVICE_RECEIVE_MODE_ENUM
---

# FAX_DEVICE_RECEIVE_MODE_ENUM enumeration


## -description

The <b>FAX_DEVICE_RECEIVE_MODE_ENUM</b> enumeration defines the way a device answers an incoming call.

## -enum-fields

### -field fdrmNO_ANSWER:0

The device will not answer the call.

### -field fdrmAUTO_ANSWER

The device will automatically answer the call.

### -field fdrmMANUAL_ANSWER

The device will answer the call only if made to do so manually.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice-receivemode">ReceiveMode</a>
