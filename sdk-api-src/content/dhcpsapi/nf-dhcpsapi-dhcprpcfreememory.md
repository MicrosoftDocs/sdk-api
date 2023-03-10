---
UID: NF:dhcpsapi.DhcpRpcFreeMemory
title: DhcpRpcFreeMemory function (dhcpsapi.h)
description: The DhcpRpcFreeMemory function frees a block of buffer space returned as a parameter.
helpviewer_keywords: ["DhcpRpcFreeMemory","DhcpRpcFreeMemory function [DHCP]","dhcp.dhcprpcfreememory","dhcpsapi/DhcpRpcFreeMemory"]
old-location: dhcp\dhcprpcfreememory.htm
tech.root: DHCP
ms.assetid: bf22a0a6-2ecd-4460-89c4-3f870c6275dc
ms.date: 12/05/2018
ms.keywords: DhcpRpcFreeMemory, DhcpRpcFreeMemory function [DHCP], dhcp.dhcprpcfreememory, dhcpsapi/DhcpRpcFreeMemory
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DhcpRpcFreeMemory
 - dhcpsapi/DhcpRpcFreeMemory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpRpcFreeMemory
---

# DhcpRpcFreeMemory function


## -description

The <b>DhcpRpcFreeMemory</b> function frees a block of buffer space returned as a parameter.

## -parameters

### -param BufferPointer

Pointer to an address that contains a structure (or structures, in the case of an array) returned as a parameter.

## -returns

This function does not return a value.

## -remarks

This function should be called to release the memory consumed by any structures.

