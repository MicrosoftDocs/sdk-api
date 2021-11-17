---
UID: NS:mstcpip._TIMESTAMPING_CONFIG
title: TIMESTAMPING_CONFIG
description: Describes the input structure used by the [SIO_TIMESTAMPING](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL to configure timestamp reception for a datagram socket.
ms.date: 10/07/2020
targetos: Windows
tech.root: winsock
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: mstcpip.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: TIMESTAMPING_CONFIG, *PTIMESTAMPING_CONFIG
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mstcpip.h
api_name:
 - _TIMESTAMPING_CONFIG
 - PTIMESTAMPING_CONFIG
 - TIMESTAMPING_CONFIG
f1_keywords:
 - _TIMESTAMPING_CONFIG
 - mstcpip/_TIMESTAMPING_CONFIG
 - PTIMESTAMPING_CONFIG
 - mstcpip/PTIMESTAMPING_CONFIG
 - TIMESTAMPING_CONFIG
 - mstcpip/TIMESTAMPING_CONFIG
dev_langs:
 - c++
---

## -description

Describes the input structure used by the [SIO_TIMESTAMPING](/windows/win32/winsock/winsock-ioctls#sio_timestamping) configuration IOCTL to configure timestamp reception for a datagram socket.

## -struct-fields

### -field Flags

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

Enable/disable timestamp reception for rx/tx direction.

Use the values **TIMESTAMPING_FLAG_RX** (0x1) and **TIMESTAMPING_FLAG_TX** (0x2) (both defined in `mstcpip.h`). Specify a value to enable timestamp reception for that direction; and omit a value to disable timestamp reception for that direction.

### -field TxTimestampsBuffered

Type: **[USHORT](/windows/win32/winprog/windows-data-types)**

Determines how many tx timestamps may be buffered. When the count of tx timestamps that have been buffered reaches a value equal to *TxTimestampsBuffered*, and a new tx timestamp has been generated, the new timestamp will be discarded.

## -remarks

## -see-also
