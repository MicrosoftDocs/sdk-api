---
UID: NS:wsrm._RM_SEND_WINDOW
title: RM_SEND_WINDOW (wsrm.h)
description: The RM_SEND_WINDOW structure specifies the Reliable Multicast send window. This structure is used with the RM_RATE_WINDOW_SIZE socket option.
helpviewer_keywords: ["RM_SEND_WINDOW","RM_SEND_WINDOW structure [Winsock]","winsock.rm_send_window","wsrm/RM_SEND_WINDOW"]
old-location: winsock\rm_send_window.htm
tech.root: WinSock
ms.assetid: 7ce84d2e-a52f-4652-b24a-55c94b7c120b
ms.date: 12/05/2018
ms.keywords: RM_SEND_WINDOW, RM_SEND_WINDOW structure [Winsock], winsock.rm_send_window, wsrm/RM_SEND_WINDOW
req.header: wsrm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: RM_SEND_WINDOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RM_SEND_WINDOW
 - wsrm/_RM_SEND_WINDOW
 - RM_SEND_WINDOW
 - wsrm/RM_SEND_WINDOW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsrm.h
api_name:
 - RM_SEND_WINDOW
---

# RM_SEND_WINDOW structure


## -description

The <b>RM_SEND_WINDOW</b> structure specifies the Reliable Multicast send window. This structure is used with the <a href="/windows/desktop/WinSock/ipproto-rm-socket-options">RM_RATE_WINDOW_SIZE</a> socket option.

## -struct-fields

### -field RateKbitsPerSec

Transmission rate for the send window, in kilobits per second.

### -field WindowSizeInMSecs

Window size for the send window, in milliseconds.

### -field WindowSizeInBytes

Window size for the session, in bytes.

## -remarks

Any combination of the three available members may be set for a given socket option call. For example, one, any two, or all three members may be specified during a <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> function call. Regardless of settings, Windows enforces the following ratio: <b>TransmissionRate</b> == (<b>WindowSizeBytes</b>/<b>WindowSizeMSecs</b>) * 8. As such, setting any two parameters effectively sets the third to ensure optimum performance. 

The combination of these members can affect the resources used on a PGM sender's computer. For example, a large transmission rate value combined with a large window size results in more required buffer space.

## -see-also

<a href="/windows/desktop/WinSock/ipproto-rm-socket-options">IPPROTO_RM Socket Options</a>



<a href="/windows/desktop/WinSock/reliable-multicast-programming--pgm-">Reliable Multicast Programming</a>



<a href="/windows/desktop/WinSock/socket-options">Socket Options</a>



<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a>