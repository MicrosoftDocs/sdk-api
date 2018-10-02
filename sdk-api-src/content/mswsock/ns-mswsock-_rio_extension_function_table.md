---
UID: NS:mswsock._RIO_EXTENSION_FUNCTION_TABLE
title: "_RIO_EXTENSION_FUNCTION_TABLE"
author: windows-sdk-content
description: Contains information on the functions that implement the Winsock registered I/O extensions.
old-location: winsock\rio_extension_function_table.htm
tech.root: WinSock
ms.assetid: 33C190B0-DE01-47A0-93AF-627FC5C5FF48
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PRIO_EXTENSION_FUNCTION_TABLE, PRIO_EXTENSION_FUNCTION_TABLE, PRIO_EXTENSION_FUNCTION_TABLE structure pointer [Winsock], RIO_EXTENSION_FUNCTION_TABLE, RIO_EXTENSION_FUNCTION_TABLE structure [Winsock], _RIO_EXTENSION_FUNCTION_TABLE, mswsockdef/PRIO_EXTENSION_FUNCTION_TABLE, mswsockdef/RIO_EXTENSION_FUNCTION_TABLE, winsock.rio_extension_function_table"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mswsock.h
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
 - RIO_EXTENSION_FUNCTION_TABLE
product: Windows
targetos: Windows
req.typenames: RIO_EXTENSION_FUNCTION_TABLE, *PRIO_EXTENSION_FUNCTION_TABLE
req.redist: 
---

# _RIO_EXTENSION_FUNCTION_TABLE structure


## -description


The <b>RIO_EXTENSION_FUNCTION_TABLE</b> structure contains information on the  functions that implement the Winsock registered I/O extensions.


## -struct-fields




### -field cbSize

The size, in bytes, of the structure.




### -field RIOReceive

A pointer to the <a href="https://msdn.microsoft.com/26726277-4907-47A1-BACF-868389B46EA8">RIOReceive</a> function.


### -field RIOReceiveEx

A pointer to the <a href="https://msdn.microsoft.com/74C006D0-EE13-4518-8ACC-C0CFD44D09A3">RIOReceiveEx</a> function.


### -field RIOSend

A pointer to the <a href="https://msdn.microsoft.com/A1CE9224-1E8C-46F8-AD7B-DBCBEBC670F7">RIOSend</a> function.


### -field RIOSendEx

A pointer to the <a href="https://msdn.microsoft.com/BD246278-C2BF-48E6-97AD-65057EDA1F59">RIOSendEx</a> function.


### -field RIOCloseCompletionQueue

A pointer to the <a href="https://msdn.microsoft.com/A5700ACD-3F4B-4AFF-8BA1-6AC59402E06C">RIOCloseCompletionQueue</a> function.


### -field RIOCreateCompletionQueue

A pointer to the <a href="https://msdn.microsoft.com/ABCA52BA-FB5F-427A-9EFA-A7AA4E8D98A4">RIOCreateCompletionQueue</a> function.


### -field RIOCreateRequestQueue

A pointer to the <a href="https://msdn.microsoft.com/CB69E0B6-519D-4268-A09B-196BBB6EB460">RIOCreateRequestQueue</a> function.


### -field RIODequeueCompletion

A pointer to the <a href="https://msdn.microsoft.com/658729C0-2963-45F0-B616-01372A7144D1">RIODequeueCompletion</a> function.


### -field RIODeregisterBuffer

A pointer to the <a href="https://msdn.microsoft.com/5D5C3469-0D5B-4E89-BE59-8D8AE9DBA5DE">RIODeregisterBuffer</a> function.


### -field RIONotify

A pointer to the <a href="https://msdn.microsoft.com/02264DAC-A3A1-4F7D-9728-17BE7F10E859">RIONotify</a> function.


### -field RIORegisterBuffer

A pointer to the <a href="https://msdn.microsoft.com/CAADCC2F-1443-410F-A860-375C9AAE208E">RIORegisterBuffer</a> function.


### -field RIOResizeCompletionQueue

A pointer to the <a href="https://msdn.microsoft.com/C3C9A6CA-2C2E-4A5F-BDE7-635DF0B93B1A">RIOResizeCompletionQueue</a> function.


### -field RIOResizeRequestQueue

A pointer to the <a href="https://msdn.microsoft.com/4A20B1E3-ED99-4429-A9C1-35C9330CB108">RIOResizeRequestQueue</a> function.


## -remarks



The <b>RIO_EXTENSION_FUNCTION_TABLE</b> structure contains information on the  functions that implement the Winsock registered I/O extensions.

The function pointers for the 
Winsock registered I/O extension functions must be obtained at run time by making a call to the 
<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> function with the <b>SIO_GET_MULTIPLE_EXTENSION_FUNCTION_POINTER</b> opcode specified. The input buffer passed to the <b>WSAIoctl</b> function must contain <b>WSAID_MULTIPLE_RIO</b>, a globally unique identifier (GUID) whose value identifies the Winsock registered I/O  extension functions. On success, the output returned by the <b>WSAIoctl</b> function contains a pointer to the <b>RIO_EXTENSION_FUNCTION_TABLE</b> structure that contains pointers to the Winsock registered I/O  extension functions. The <b>SIO_GET_MULTIPLE_EXTENSION_FUNCTION_POINTER</b> IOCTL is defined in the <i>Ws2def.h</i> header file.The <b>WSAID_MULTIPLE_RIO</b> GUID is defined in the <i>Mswsock.h</i> header file.




## -see-also




<a href="https://msdn.microsoft.com/A5700ACD-3F4B-4AFF-8BA1-6AC59402E06C">RIOCloseCompletionQueue</a>



<a href="https://msdn.microsoft.com/ABCA52BA-FB5F-427A-9EFA-A7AA4E8D98A4">RIOCreateCompletionQueue</a>



<a href="https://msdn.microsoft.com/CB69E0B6-519D-4268-A09B-196BBB6EB460">RIOCreateRequestQueue</a>



<a href="https://msdn.microsoft.com/658729C0-2963-45F0-B616-01372A7144D1">RIODequeueCompletion</a>



<a href="https://msdn.microsoft.com/5D5C3469-0D5B-4E89-BE59-8D8AE9DBA5DE">RIODeregisterBuffer</a>



<a href="https://msdn.microsoft.com/02264DAC-A3A1-4F7D-9728-17BE7F10E859">RIONotify</a>



<a href="https://msdn.microsoft.com/26726277-4907-47A1-BACF-868389B46EA8">RIOReceive</a>



<a href="https://msdn.microsoft.com/74C006D0-EE13-4518-8ACC-C0CFD44D09A3">RIOReceiveEx</a>



<a href="https://msdn.microsoft.com/CAADCC2F-1443-410F-A860-375C9AAE208E">RIORegisterBuffer</a>



<a href="https://msdn.microsoft.com/C3C9A6CA-2C2E-4A5F-BDE7-635DF0B93B1A">RIOResizeCompletionQueue</a>



<a href="https://msdn.microsoft.com/4A20B1E3-ED99-4429-A9C1-35C9330CB108">RIOResizeRequestQueue</a>



<a href="https://msdn.microsoft.com/A1CE9224-1E8C-46F8-AD7B-DBCBEBC670F7">RIOSend</a>



<a href="https://msdn.microsoft.com/BD246278-C2BF-48E6-97AD-65057EDA1F59">RIOSendEx</a>



<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a>
 

 

