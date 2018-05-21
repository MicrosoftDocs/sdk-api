---
UID: NS:combaseapi.tagServerInformation
title: tagServerInformation
author: windows-driver-content
description: Represents the implementation of a Component Object Model (COM) interface in a server process.
old-location: winrt\serverinformation.htm
old-project: WinRT
ms.assetid: 568246B8-48F7-4A83-B7DE-24F36B2C3F49
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: "*PServerInformation, PServerInformation, PServerInformation structure pointer [Windows Runtime], ServerInformation, ServerInformation structure [Windows Runtime], combaseapi/PServerInformation, combaseapi/ServerInformation, tagServerInformation, winrt.serverinformation"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: combaseapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ServerInformation, *PServerInformation
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	combaseapi.h
api_name:
-	ServerInformation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagServerInformation structure


## -description


Represents the implementation of a Component Object Model (COM) interface in a server process. 


## -struct-fields




### -field dwServerPid

The process ID of the server.


### -field dwServerTid

The thread ID of the server object if it's in the STA, 0 if it's in the MTA, and <b>0x0000FFFF</b> if it's in the NA.


### -field ui64ServerAddress

<i>ui64ServerAddress</i> is considered a 64-bit value type, rather than a pointer  to a 64-bit value, and isn't a pointer to an object in the debugger process. Instead, this address is passed to the <a href="https://msdn.microsoft.com/8774e145-ee7f-44de-85db-0445b905f986">ReadProcessMemory</a> function.


## -remarks



The <b>ServerInformation</b> structure is used by the <a href="https://msdn.microsoft.com/C61C68B1-78CA-4052-9E24-629AB4083B86">CoDecodeProxy</a> function to enable native debuggers to locate the implementation of a COM interface in a server process, given a Windows Runtime interface on a proxy to the Windows Runtime object.





## -see-also




<a href="https://msdn.microsoft.com/C61C68B1-78CA-4052-9E24-629AB4083B86">CoDecodeProxy</a>
 

 

