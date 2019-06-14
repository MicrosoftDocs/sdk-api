---
UID: NF:msajtransport.AllJoynEnumEvents
title: AllJoynEnumEvents function (msajtransport.h)
author: windows-sdk-content
description: Provides AllJoyn transport functionality similar to the TCP socket WSAEnumNetworkEvents functionality.
old-location: alljoyn\alljoynenumevents.htm
tech.root: AllJoyn
ms.assetid: 0B53EAE5-9043-46F2-9C7B-A5836AF241A3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AllJoynEnumEvents, AllJoynEnumEvents function [AllJoyn API], alljoyn.alljoynenumevents, msajtransport/AllJoynEnumEvents
ms.topic: function
req.header: msajtransport.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: MSAJApi.lib
req.dll: MSAJApi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - MSAJApi.dll
api_name:
 - AllJoynEnumEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AllJoynEnumEvents function


## -description


Provides AllJoyn transport functionality similar to the TCP socket <a href="https://docs.microsoft.com/windows/desktop/api/winsock2/nf-winsock2-wsaenumnetworkevents">WSAEnumNetworkEvents</a>  functionality.


## -parameters




### -param connectedBusHandle [in]

Pipe handle.


### -param eventToReset [in, optional]

Optional handle to the event to be reset after completion of this call.


### -param eventTypes [out]

Output for bitmask of events being set.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.



