---
UID: NF:nspapi.GetNameByTypeA
title: GetNameByTypeA function
author: windows-sdk-content
description: The GetNameByType function retrieves the name of a network service for the specified service type.
old-location: winsock\getnamebytype_2.htm
tech.root: winsock
ms.assetid: 74d747f0-5f5e-4f54-8b2f-7ea96d4043ee
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetNameByType, GetNameByType function [Winsock], GetNameByTypeA, GetNameByTypeW, _win32_getnamebytype_2, nspapi/GetNameByType, nspapi/GetNameByTypeA, nspapi/GetNameByTypeW, winsock.getnamebytype_2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: nspapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetNameByTypeW (Unicode) and GetNameByTypeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mswsock.lib
req.dll: Mswsock.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mswsock.dll
api_name:
 - GetNameByType
 - GetNameByTypeA
 - GetNameByTypeW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetNameByTypeA function


## -description


The 
<b>GetNameByType</b> function retrieves the name of a network service for the specified service type.


<div class="alert"><b>Note</b>  The 
<b>GetNameByType</b> function is a Microsoft-specific extension to the Windows Sockets 1.1 specification. This function is obsolete. For the convenience of Windows Sockets 1.1 developers, the reference material is as follows.</div>
<div> </div>



<div class="alert"><b>Note</b>  The functions detailed in 
<a href="https://msdn.microsoft.com/f55219b9-1518-4b49-a0da-6a3fa025cca3">Protocol-Independent Name Resolution</a> provide equivalent functionality in Windows Sockets 2.</div>
<div> </div>



## -parameters




### -param lpServiceType [in]

A pointer to a globally unique identifier (GUID) that specifies the type of the network service. The <i>Svcguid.h</i> header file includes definitions of several GUID service types, and macros for working with them.

The <i>Svcguid.h</i> header file is not automatically included by the <i>Winsock2.h</i> header file.


### -param lpServiceName [out]

A pointer to a buffer to receive a zero-terminated string that uniquely represents the name of the network service.


### -param dwNameLength [in]

A pointer to a variable that, on input, specifies the size, in bytes, of the buffer pointed to by <i>lpServiceName</i>. On output, the variable contains the actual size of the service name string, in bytes.


## -returns



If the function succeeds, the return value is not SOCKET_ERROR (–1).

If the function fails, the return value is SOCKET_ERROR (–1). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/177bbae5-bc00-4ce5-a0f7-8474f0c2cb2e">GetTypeByName</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>
 

 

