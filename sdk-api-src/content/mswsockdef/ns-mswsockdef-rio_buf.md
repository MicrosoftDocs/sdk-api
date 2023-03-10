---
UID: NS:mswsockdef._RIO_BUF
title: RIO_BUF (mswsockdef.h)
description: Specifies a portion of a registered buffer used for sending or receiving network data with the Winsock registered I/O extensions.
helpviewer_keywords: ["*PRIO_BUF","PRIO_BUF","PRIO_BUF structure pointer [Winsock]","RIO_BUF","RIO_BUF structure [Winsock]","mswsockdef/PRIO_BUF","mswsockdef/RIO_BUF","winsock.rio_buf"]
old-location: winsock\rio_buf.htm
tech.root: WinSock
ms.assetid: DD55194E-EE66-4FD4-87BC-E855922CEEA1
ms.date: 12/05/2018
ms.keywords: '*PRIO_BUF, PRIO_BUF, PRIO_BUF structure pointer [Winsock], RIO_BUF, RIO_BUF structure [Winsock], mswsockdef/PRIO_BUF, mswsockdef/RIO_BUF, winsock.rio_buf'
req.header: mswsockdef.h
req.include-header: Mswsock.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: RIO_BUF, *PRIO_BUF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RIO_BUF
 - mswsockdef/_RIO_BUF
 - PRIO_BUF
 - mswsockdef/PRIO_BUF
 - RIO_BUF
 - mswsockdef/RIO_BUF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mswsockdef.h
api_name:
 - RIO_BUF
---

# RIO_BUF structure


## -description

The <b>RIO_BUF</b> structure specifies a portion of a registered buffer used for sending or receiving network data with the Winsock registered I/O extensions.

## -struct-fields

### -field BufferId

The registered buffer descriptor for a Winsock registered I/O buffer used with send and receive requests.

### -field Offset

The offset, in bytes, into the buffer specified by the <b>BufferId</b> member. An <b>Offset</b> value of zero points to the beginning of the buffer

### -field Length

A length, in bytes, of the buffer to use from the <b>Offset</b> member.

## -remarks

The Winsock registered I/O extensions often operate on portions of registered buffers sometimes called buffer slices. The <b>RIO_BUF</b> structure is used by an application that needs to use a small amount of registered memory for sending or receiving network data. The application can often increase performance by registering one large buffer and then using small chunks of the buffer as needed. The <b>RIO_BUF</b> structure may describe any contiguous segment of memory contained in a single buffer registration.

A pointer to a <b>RIO_BUF</b> structure is passed as the <i>pData</i> parameter to the <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend">RIOSend</a>,  <a href="/previous-versions/windows/desktop/legacy/hh437216(v=vs.85)">RIOSendEx</a>, <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive">RIOReceive</a>, and <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex">RIOReceiveEx</a> functions to send or receive network data.

An application cannot resize a registered buffer simply by using a buffer slice with values larger than the original buffer that was registered using the <a href="/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)">RIORegisterBuffer</a> function.

The <b>RIO_BUF</b> structure is defined in the <i>Mswsockdef.h</i> header file which is automatically included in the <i>Mswsock.h</i> header file. The <i>Mswsockdef.h</i> header file should never be used directly.

## -see-also

<a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer">RIODeregisterBuffer</a>



<a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive">RIOReceive</a>



<a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex">RIOReceiveEx</a>



<a href="/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)">RIORegisterBuffer</a>



<a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend">RIOSend</a>



<a href="/previous-versions/windows/desktop/legacy/hh437216(v=vs.85)">RIOSendEx</a>



<a href="/windows/desktop/WinSock/rio-bufferid">RIO_BUFFERID</a>