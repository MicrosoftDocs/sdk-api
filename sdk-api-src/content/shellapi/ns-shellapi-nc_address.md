---
UID: NS:shellapi.tagNC_ADDRESS
title: NC_ADDRESS (shellapi.h)
description: Contains information that describes a network address.
helpviewer_keywords: ["*PNC_ADDRESS","NC_ADDRESS","NC_ADDRESS structure [Windows Shell]","PNC_ADDRESS","PNC_ADDRESS structure pointer [Windows Shell]","_shell_NC_ADDRESS","shell.NC_ADDRESS","shellapi/NC_ADDRESS","shellapi/PNC_ADDRESS"]
old-location: shell\NC_ADDRESS.htm
tech.root: shell
ms.assetid: 1dfb0f6a-3aa5-486b-bbd0-8a24070bca19
ms.date: 12/05/2018
ms.keywords: '*PNC_ADDRESS, NC_ADDRESS, NC_ADDRESS structure [Windows Shell], PNC_ADDRESS, PNC_ADDRESS structure pointer [Windows Shell], _shell_NC_ADDRESS, shell.NC_ADDRESS, shellapi/NC_ADDRESS, shellapi/PNC_ADDRESS'
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
targetos: Windows
req.typenames: NC_ADDRESS, *PNC_ADDRESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNC_ADDRESS
 - shellapi/tagNC_ADDRESS
 - PNC_ADDRESS
 - shellapi/PNC_ADDRESS
 - NC_ADDRESS
 - shellapi/NC_ADDRESS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shellapi.h
api_name:
 - NC_ADDRESS
---

# NC_ADDRESS structure


## -description

Contains information that describes a network address.

## -struct-fields

### -field pAddrInfo

Type: <b><a href="/windows/desktop/shell/hkey-type">NET_ADDRESS_INFO</a>*</b>

A pointer to a <a href="/windows/desktop/shell/hkey-type">NET_ADDRESS_INFO</a>  structure that describes the network address, either a named address or an IP address.

### -field PortNumber

Type: <b>USHORT</b>

The network port number, if the address described by <b>pAddrInfo</b> is an IP address.

### -field PrefixLength

Type: <b>BYTE</b>

The prefix length corresponding to the address, if the address described by <b>pAddrInfo</b> is an IP address.

## -remarks

This structure is sent with the <a href="/windows/desktop/api/shellapi/nf-shellapi-netaddr_getaddress">NetAddr_GetAddress</a> macro.