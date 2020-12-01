---
UID: NS:qossp._QOS_DESTADDR
title: QOS_DESTADDR (qossp.h)
description: The QOS object QOS_DESTADDR is used during a call to the WSAIoctl (SIO_SET_QOS) function in order to avoid issuing a connect function call for a sending socket.
helpviewer_keywords: ["*LPQOS_DESTADDR","LPQOS_DESTADDR","LPQOS_DESTADDR structure pointer [QOS]","QOS_DESTADDR","QOS_DESTADDR structure [QOS]","_gqos_qos_destaddr","qos.qos_destaddr","qossp/LPQOS_DESTADDR","qossp/QOS_DESTADDR"]
old-location: qos\qos_destaddr.htm
tech.root: QOS
ms.assetid: 6b9e52b2-58d0-437f-a71b-248feac59c13
ms.date: 12/05/2018
ms.keywords: '*LPQOS_DESTADDR, LPQOS_DESTADDR, LPQOS_DESTADDR structure pointer [QOS], QOS_DESTADDR, QOS_DESTADDR structure [QOS], _gqos_qos_destaddr, qos.qos_destaddr, qossp/LPQOS_DESTADDR, qossp/QOS_DESTADDR'
req.header: qossp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: QOS_DESTADDR, *LPQOS_DESTADDR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QOS_DESTADDR
 - qossp/_QOS_DESTADDR
 - LPQOS_DESTADDR
 - qossp/LPQOS_DESTADDR
 - QOS_DESTADDR
 - qossp/QOS_DESTADDR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qossp.h
api_name:
 - QOS_DESTADDR
---

# QOS_DESTADDR structure


## -description

The QOS object 
<b>QOS_DESTADDR</b> is used during a call to the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> (SIO_SET_QOS) function in order to avoid issuing a <b>connect</b> function call for a sending socket.

## -struct-fields

### -field ObjectHdr

The QOS object 
<a href="/previous-versions/windows/desktop/api/qos/ns-qos-qos_object_hdr">QOS_OBJECT_HDR</a>. The object type for this QOS object should be 
<b>QOS_DESTADDR</b>.

### -field SocketAddress

Address of the destination socket.

### -field sockaddr

### -field SocketAddressLength

Length of the <b>SocketAddress</b> structure.

## -see-also

<a href="/previous-versions/windows/desktop/api/qos/ns-qos-qos_object_hdr">QOS_OBJECT_HDR</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a>