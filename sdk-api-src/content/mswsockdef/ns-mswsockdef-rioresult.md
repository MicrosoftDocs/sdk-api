---
UID: NS:mswsockdef._RIORESULT
title: RIORESULT
author: windows-sdk-content
description: Contains data used to indicate request completion results used with the Winsock registered I/O extensions.
old-location: winsock\rioresult.htm
tech.root: winsock
ms.assetid: D56D67C4-B455-4F59-8996-CF158DDA3AC2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PRIORESULT, PRIORESULT, PRIORESULT structure pointer [Winsock], RIORESULT, RIORESULT structure [Winsock], mswsockdef/PRIORESULT, mswsockdef/RIORESULT, winsock.rioresult"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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

An application-provided context specified in call to the <a href="https://msdn.microsoft.com/CB69E0B6-519D-4268-A09B-196BBB6EB460">RIOCreateRequestQueue</a> function.


### -field RequestContext

An application-provided context specified with the registered I/O request to the <a href="https://msdn.microsoft.com/26726277-4907-47A1-BACF-868389B46EA8">RIOReceive</a>, <a href="https://msdn.microsoft.com/74C006D0-EE13-4518-8ACC-C0CFD44D09A3">RIOReceiveEx</a>, <a href="https://msdn.microsoft.com/A1CE9224-1E8C-46F8-AD7B-DBCBEBC670F7">RIOSend</a>, and  <a href="https://msdn.microsoft.com/BD246278-C2BF-48E6-97AD-65057EDA1F59">RIOSendEx</a> functions.


## -remarks



The <b>RIORESULT</b> structure defines the data format used to indicate request completion by the Winsock registered I/O extensions.  An application requests completion indications by allocating an array of <b>RIORESULT</b> structures  and passing the array of <b>RIORESULT</b> structures to the <a href="https://msdn.microsoft.com/658729C0-2963-45F0-B616-01372A7144D1">RIODequeueCompletion</a> function along with the element count.  The application need not perform any initialization of the <b>RIORESULT</b> structure elements before calling the <b>RIODequeueCompletion</b> function.

The <b>SocketContext</b> member of the <b>RIORESULT</b> structure can be used by an application to identify the <a href="https://msdn.microsoft.com/9196F8AF-3C48-445D-B2D5-E22A99759D92">RIO_CQ</a> object or the associated application object on which the Winsock registered I/O request was issued.  The <b>RequestContext</b> member of the <b>RIORESULT</b> structure can similarly be used to identify the particular Winsock registered I/O request that was completed.

The <b>RIORESULT</b> structure is defined in the <i>Mswsockdef.h</i> header file which is automatically included in the <i>Mswsock.h</i> header file. The <i>Mswsockdef.h</i> header file should never be used directly.





## -see-also




<a href="https://msdn.microsoft.com/CB69E0B6-519D-4268-A09B-196BBB6EB460">RIOCreateRequestQueue</a>



<a href="https://msdn.microsoft.com/658729C0-2963-45F0-B616-01372A7144D1">RIODequeueCompletion</a>



<a href="https://msdn.microsoft.com/26726277-4907-47A1-BACF-868389B46EA8">RIOReceive</a>



<a href="https://msdn.microsoft.com/74C006D0-EE13-4518-8ACC-C0CFD44D09A3">RIOReceiveEx</a>



<a href="https://msdn.microsoft.com/A1CE9224-1E8C-46F8-AD7B-DBCBEBC670F7">RIOSend</a>



<a href="https://msdn.microsoft.com/BD246278-C2BF-48E6-97AD-65057EDA1F59">RIOSendEx</a>
 

 

