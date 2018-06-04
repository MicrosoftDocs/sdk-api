---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _TCPIP_OWNER_MODULE_BASIC_INFO structure


## -description


The <b>TCPIP_OWNER_MODULE_BASIC_INFO</b> structure contains pointers to the module name and module path values associated with a TCP connection. The <b>TCPIP_OWNER_MODULE_BASIC_INFO</b> structure is returned by the <a href="https://msdn.microsoft.com/12162f0a-56c1-4f81-a1f5-3cd5ad975d0d">GetOwnerModuleFromTcpEntry</a> and <a href="https://msdn.microsoft.com/021679fc-91de-4e3b-956d-bb00b1856f20">GetOwnerModuleFromTcp6Entry</a> functions.


## -struct-fields




### -field pModuleName

A pointer to the name of the module. This field should be a <b>NULL</b> pointer when passed to <a href="https://msdn.microsoft.com/12162f0a-56c1-4f81-a1f5-3cd5ad975d0d">GetOwnerModuleFromTcpEntry</a> or <a href="https://msdn.microsoft.com/021679fc-91de-4e3b-956d-bb00b1856f20">GetOwnerModuleFromTcp6Entry</a> function.


### -field pModulePath

A pointer to the full path of the module, including the module name. This field should be a <b>NULL</b> pointer when passed to <a href="https://msdn.microsoft.com/12162f0a-56c1-4f81-a1f5-3cd5ad975d0d">GetOwnerModuleFromTcpEntry</a> or <a href="https://msdn.microsoft.com/021679fc-91de-4e3b-956d-bb00b1856f20">GetOwnerModuleFromTcp6Entry</a> function.


## -remarks



If the module owner is the system kernel, the <b>lpModuleName</b> and <b>lpModulePath</b> members point to a wide character string that contains "System".

On Windows Vista and later as well as on the Microsoft Windows Software Development Kit (SDK), the organization of header files has changed and the <b>TCPIP_OWNER_MODULE_BASIC_INFO</b> structure is defined in the <i>Iprtrmib.h</i> header file. 



