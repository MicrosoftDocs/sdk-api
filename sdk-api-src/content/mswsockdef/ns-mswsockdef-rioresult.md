---
UID: NS:mswsockdef._RIORESULT
title: RIORESULT (mswsockdef.h)
author: windows-sdk-content
description: Contains data used to indicate request completion results used with the Winsock registered I/O extensions.
old-location: winsock\rioresult.htm
tech.root: WinSock
ms.assetid: D56D67C4-B455-4F59-8996-CF158DDA3AC2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PRIORESULT, PRIORESULT, PRIORESULT structure pointer [Winsock], RIORESULT, RIORESULT structure [Winsock], mswsockdef/PRIORESULT, mswsockdef/RIORESULT, winsock.rioresult"
ms.topic: struct
f1_keywords: 
 - "mswsockdef/RIORESULT"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mswsockdef.h
api_name:
 - RIORESULT
product: Windows
targetos: Windows
req.typenames: RIORESULT, *PRIORESULT
req.redist: 
ms.custom: 19H1
---

# RIORESULT structure


## -description


The <b>RIORESULT</b> structure contains data used to indicate request completion  results used with the Winsock registered I/O extensions.


## -struct-fields




### -field Status

The completion status of the Winsock registered I/O request.


### -field BytesTransferred

The number of bytes sent or received in the I/O request.


### -field SocketContext

An application-provided context specified in call to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh448843(v=vs.85)">RIOCreateRequestQueue</a> function.


### -field RequestContext

An application-provided context specified with the registered I/O request to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437193(v=vs.85)">RIOReceive</a>, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437196(v=vs.85)">RIOReceiveEx</a>, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437213(v=vs.85)">RIOSend</a>, and  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437216(v=vs.85)">RIOSendEx</a> functions.


## -remarks



The <b>RIORESULT</b> structure defines the data format used to indicate request completion by the Winsock registered I/O extensions.  An application requests completion indications by allocating an array of <b>RIORESULT</b> structures  and passing the array of <b>RIORESULT</b> structures to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh448845(v=vs.85)">RIODequeueCompletion</a> function along with the element count.  The application need not perform any initialization of the <b>RIORESULT</b> structure elements before calling the <b>RIODequeueCompletion</b> function.

The <b>SocketContext</b> member of the <b>RIORESULT</b> structure can be used by an application to identify the <a href="https://docs.microsoft.com/windows/desktop/WinSock/riocqueue">RIO_CQ</a> object or the associated application object on which the Winsock registered I/O request was issued.  The <b>RequestContext</b> member of the <b>RIORESULT</b> structure can similarly be used to identify the particular Winsock registered I/O request that was completed.

The <b>RIORESULT</b> structure is defined in the <i>Mswsockdef.h</i> header file which is automatically included in the <i>Mswsock.h</i> header file. The <i>Mswsockdef.h</i> header file should never be used directly.





## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh448843(v=vs.85)">RIOCreateRequestQueue</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh448845(v=vs.85)">RIODequeueCompletion</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437193(v=vs.85)">RIOReceive</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437196(v=vs.85)">RIOReceiveEx</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437213(v=vs.85)">RIOSend</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437216(v=vs.85)">RIOSendEx</a>
 

 

