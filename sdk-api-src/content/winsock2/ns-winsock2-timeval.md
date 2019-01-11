---
UID: NS:winsock2.timeval
title: TIMEVAL
author: windows-sdk-content
description: The timeval structure is used to specify a time interval. It is associated with the Berkeley Software Distribution (BSD) Time.h header file.
old-location: winsock\timeval_2.htm
tech.root: WinSock
ms.assetid: 3024c961-bb47-40ac-a49c-b12cd431e4e7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPTIMEVAL, *PTIMEVAL, TIMEVAL, _win32_timeval_2, timeval, timeval structure [Winsock], winsock.timeval_2, winsock/timeval"
ms.topic: struct
req.header: winsock2.h
req.include-header: Winsock2.h
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
 - winsock.h
api_name:
 - timeval
product: Windows
targetos: Windows
req.typenames: TIMEVAL, *PTIMEVAL, *LPTIMEVAL
req.redist: 
---

# TIMEVAL structure


## -description


The 
<b>timeval</b> structure is used to specify a time interval. It is associated with the Berkeley Software Distribution (BSD) <i>Time.h</i> header file.


## -struct-fields




### -field tv_sec

Time interval, in seconds.


### -field tv_usec

Time interval, in microseconds. This value is used in combination with the <b>tv_sec</b> member to represent time interval values  that are not a multiple of seconds. 


## -remarks



The <b>timeval</b> structure is used in Windows Sockets by the <a href="https://msdn.microsoft.com/f9f1092d-7e15-41cd-a42f-abe8a4f33e15">select</a> function to specify the maximum time the function can take to complete. The time interval is a combination of the values in <b>tv_sec</b> and <b>tv_usec</b> members.

Several functions are added on Windows Vista and later that use the  <b>timeval</b> structure. These functions include <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>, <a href="https://msdn.microsoft.com/6d3c5b97-32ce-4eb5-a047-d9b37c37cdda">SetAddrInfoEx</a>, <a href="https://msdn.microsoft.com/7323d814-e96e-44b9-8ade-a9317e4fbf17">WSAConnectByList</a>, and <a href="https://msdn.microsoft.com/6d87699f-03bd-4579-9907-ae3c29b7332b">WSAConnectByName</a>. 




## -see-also




<a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>



<a href="https://msdn.microsoft.com/6d3c5b97-32ce-4eb5-a047-d9b37c37cdda">SetAddrInfoEx</a>



<a href="https://msdn.microsoft.com/7323d814-e96e-44b9-8ade-a9317e4fbf17">WSAConnectByList</a>



<a href="https://msdn.microsoft.com/6d87699f-03bd-4579-9907-ae3c29b7332b">WSAConnectByName</a>



<a href="https://msdn.microsoft.com/c1dbabcf-b5cd-4a9d-9bf9-b04c62117d74">linger</a>



<a href="https://msdn.microsoft.com/f9f1092d-7e15-41cd-a42f-abe8a4f33e15">select</a>
 

 

