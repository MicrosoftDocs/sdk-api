---
UID: NS:combaseapi.tagServerInformation
title: ServerInformation (combaseapi.h)
description: Represents the implementation of a Component Object Model (COM) interface in a server process.
helpviewer_keywords: ["*PServerInformation","PServerInformation","PServerInformation structure pointer [Windows Runtime]","ServerInformation","ServerInformation structure [Windows Runtime]","combaseapi/PServerInformation","combaseapi/ServerInformation","winrt.serverinformation"]
old-location: winrt\serverinformation.htm
tech.root: WinRT
ms.assetid: 568246B8-48F7-4A83-B7DE-24F36B2C3F49
ms.date: 12/05/2018
ms.keywords: '*PServerInformation, PServerInformation, PServerInformation structure pointer [Windows Runtime], ServerInformation, ServerInformation structure [Windows Runtime], combaseapi/PServerInformation, combaseapi/ServerInformation, winrt.serverinformation'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ServerInformation, *PServerInformation
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagServerInformation
 - combaseapi/tagServerInformation
 - PServerInformation
 - combaseapi/PServerInformation
 - ServerInformation
 - combaseapi/ServerInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - combaseapi.h
api_name:
 - ServerInformation
---

# ServerInformation structure


## -description

Represents the implementation of a Component Object Model (COM) interface in a server process.

## -struct-fields

### -field dwServerPid

The process ID of the server.

### -field dwServerTid

The thread ID of the server object if it's in the STA, 0 if it's in the MTA, and <b>0x0000FFFF</b> if it's in the NA.

### -field ui64ServerAddress

<i>ui64ServerAddress</i> is considered a 64-bit value type, rather than a pointer  to a 64-bit value, and isn't a pointer to an object in the debugger process. Instead, this address is passed to the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-readprocessmemory">ReadProcessMemory</a> function.

## -remarks

The <b>ServerInformation</b> structure is used by the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-codecodeproxy">CoDecodeProxy</a> function to enable native debuggers to locate the implementation of a COM interface in a server process, given a Windows Runtime interface on a proxy to the Windows Runtime object.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-codecodeproxy">CoDecodeProxy</a>