---
UID: NS:mswsockdef._RIO_BUF
title: RIO_BUF (mswsockdef.h)
author: windows-sdk-content
description: Specifies a portion of a registered buffer used for sending or receiving network data with the Winsock registered I/O extensions.
old-location: winsock\rio_buf.htm
tech.root: WinSock
ms.assetid: DD55194E-EE66-4FD4-87BC-E855922CEEA1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PRIO_BUF, PRIO_BUF, PRIO_BUF structure pointer [Winsock], RIO_BUF, RIO_BUF structure [Winsock], mswsockdef/PRIO_BUF, mswsockdef/RIO_BUF, winsock.rio_buf"
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
 - RIO_BUF
product: Windows
targetos: Windows
req.typenames: RIO_BUF, *PRIO_BUF
req.redist: 
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

A pointer to a <b>RIO_BUF</b> structure is passed as the <i>pData</i> parameter to the <a href="https://msdn.microsoft.com/A1CE9224-1E8C-46F8-AD7B-DBCBEBC670F7">RIOSend</a>,  <a href="https://msdn.microsoft.com/BD246278-C2BF-48E6-97AD-65057EDA1F59">RIOSendEx</a>, <a href="https://msdn.microsoft.com/26726277-4907-47A1-BACF-868389B46EA8">RIOReceive</a>, and <a href="https://msdn.microsoft.com/74C006D0-EE13-4518-8ACC-C0CFD44D09A3">RIOReceiveEx</a> functions to send or receive network data.

An application cannot resize a registered buffer simply by using a buffer slice with values larger than the original buffer that was registered using the <a href="https://msdn.microsoft.com/CAADCC2F-1443-410F-A860-375C9AAE208E">RIORegisterBuffer</a> function.

The <b>RIO_BUF</b> structure is defined in the <i>Mswsockdef.h</i> header file which is automatically included in the <i>Mswsock.h</i> header file. The <i>Mswsockdef.h</i> header file should never be used directly.





## -see-also




<a href="https://msdn.microsoft.com/5D5C3469-0D5B-4E89-BE59-8D8AE9DBA5DE">RIODeregisterBuffer</a>



<a href="https://msdn.microsoft.com/26726277-4907-47A1-BACF-868389B46EA8">RIOReceive</a>



<a href="https://msdn.microsoft.com/74C006D0-EE13-4518-8ACC-C0CFD44D09A3">RIOReceiveEx</a>



<a href="https://msdn.microsoft.com/CAADCC2F-1443-410F-A860-375C9AAE208E">RIORegisterBuffer</a>



<a href="https://msdn.microsoft.com/A1CE9224-1E8C-46F8-AD7B-DBCBEBC670F7">RIOSend</a>



<a href="https://msdn.microsoft.com/BD246278-C2BF-48E6-97AD-65057EDA1F59">RIOSendEx</a>



<a href="https://msdn.microsoft.com/87D0A3F6-A44C-4D7F-B276-7FD5DC2DE7A3">RIO_BUFFERID</a>
 

 

