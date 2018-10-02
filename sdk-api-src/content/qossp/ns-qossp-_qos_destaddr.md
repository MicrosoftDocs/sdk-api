---
UID: NS:qossp._QOS_DESTADDR
title: "_QOS_DESTADDR"
author: windows-sdk-content
description: The QOS object QOS_DESTADDR is used during a call to the WSAIoctl (SIO_SET_QOS) function in order to avoid issuing a connect function call for a sending socket.
old-location: qos\qos_destaddr.htm
tech.root: QOS
ms.assetid: 6b9e52b2-58d0-437f-a71b-248feac59c13
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPQOS_DESTADDR, LPQOS_DESTADDR, LPQOS_DESTADDR structure pointer [QOS], QOS_DESTADDR, QOS_DESTADDR structure [QOS], _QOS_DESTADDR, _gqos_qos_destaddr, qos.qos_destaddr, qossp/LPQOS_DESTADDR, qossp/QOS_DESTADDR"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qossp.h
api_name:
 - QOS_DESTADDR
product: Windows
targetos: Windows
req.typenames: QOS_DESTADDR, *LPQOS_DESTADDR
req.redist: 
---

# _QOS_DESTADDR structure


## -description


The QOS object 
<b>QOS_DESTADDR</b> is used during a call to the 
<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> (SIO_SET_QOS) function in order to avoid issuing a <b>connect</b> function call for a sending socket.


## -struct-fields




### -field ObjectHdr

The QOS object 
<a href="https://msdn.microsoft.com/a2021d70-e7ef-4c2a-8800-1a1d7540ce02">QOS_OBJECT_HDR</a>. The object type for this QOS object should be 
<b>QOS_DESTADDR</b>.


### -field SocketAddress

Address of the destination socket.


### -field sockaddr

 


### -field SocketAddressLength

Length of the <b>SocketAddress</b> structure.


## -see-also




<a href="https://msdn.microsoft.com/a2021d70-e7ef-4c2a-8800-1a1d7540ce02">QOS_OBJECT_HDR</a>



<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a>
 

 

