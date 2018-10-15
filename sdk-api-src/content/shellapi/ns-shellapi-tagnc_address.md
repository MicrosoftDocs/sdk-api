---
UID: NS:shellapi.tagNC_ADDRESS
title: tagNC_ADDRESS
author: windows-sdk-content
description: Contains information that describes a network address.
old-location: shell\NC_ADDRESS.htm
tech.root: shell
ms.assetid: 1dfb0f6a-3aa5-486b-bbd0-8a24070bca19
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: "*PNC_ADDRESS, NC_ADDRESS, NC_ADDRESS structure [Windows Shell], PNC_ADDRESS, PNC_ADDRESS structure pointer [Windows Shell], _shell_NC_ADDRESS, shell.NC_ADDRESS, shellapi/NC_ADDRESS, shellapi/PNC_ADDRESS, tagNC_ADDRESS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Shellapi.h
api_name:
 - NC_ADDRESS
product: Windows
targetos: Windows
req.typenames: NC_ADDRESS, *PNC_ADDRESS
req.redist: 
---

# tagNC_ADDRESS structure


## -description


Contains information that describes a network address.


## -struct-fields




### -field pAddrInfo

Type: <b><a href="https://msdn.microsoft.com/1fcb7cf5-2eff-4ff8-8cb4-00ce8dddc081">NET_ADDRESS_INFO</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/1fcb7cf5-2eff-4ff8-8cb4-00ce8dddc081">NET_ADDRESS_INFO</a>  structure that describes the network address, either a named address or an IP address.


### -field PortNumber

Type: <b>USHORT</b>

The network port number, if the address described by <b>pAddrInfo</b> is an IP address.


### -field PrefixLength

Type: <b>BYTE</b>

The prefix length corresponding to the address, if the address described by <b>pAddrInfo</b> is an IP address.


## -remarks



This structure is sent with the <a href="https://msdn.microsoft.com/2d0310a8-89ca-41b5-8afc-faec29bd23ba">NetAddr_GetAddress</a> macro.



