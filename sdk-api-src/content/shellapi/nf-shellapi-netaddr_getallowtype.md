---
UID: NF:shellapi.NetAddr_GetAllowType
title: NetAddr_GetAllowType macro (shellapi.h)
description: Retrieves the network address types that a specified network address control accepts.
helpviewer_keywords: ["NetAddr_GetAllowType","NetAddr_GetAllowType macro [Windows Shell]","_shell_NetAddr_GetAllowType","shell.NetAddr_GetAllowType","shellapi/NetAddr_GetAllowType"]
old-location: shell\NetAddr_GetAllowType.htm
tech.root: shell
ms.assetid: 21533513-86c2-418b-ab62-3c1b2db9bc2f
ms.date: 07/01/2025
ms.keywords: NetAddr_GetAllowType, NetAddr_GetAllowType macro [Windows Shell], _shell_NetAddr_GetAllowType, shell.NetAddr_GetAllowType, shellapi/NetAddr_GetAllowType
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetAddr_GetAllowType
 - shellapi/NetAddr_GetAllowType
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
 - NetAddr_GetAllowType
---

# NetAddr_GetAllowType macro

## -syntax

```cpp
DWORD NetAddr_GetAllowType(
  [in]  HWND hwnd
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns the allowed network address types as one or more of the <a href="/windows/desktop/shell/net-string">NET_STRING</a> constants.


## -description

Retrieves the network address types that a specified network address control accepts.

## -parameters

### -param hwnd [in]

A handle to the network address control.

## -remarks

The returned mask is the criterion used to validate a network address in the macro <a href="/windows/desktop/api/shellapi/nf-shellapi-netaddr_getaddress">NetAddr_GetAddress</a>.

Use this macro for a network address control only. To instantiate, use the class <b>msctls_netaddress</b> defined in Shellapi.h. Call <a href="/windows/desktop/api/shellapi/nf-shellapi-initnetworkaddresscontrol">InitNetworkAddressControl</a> at run time before calling this macro. This initializes the common controls library that contains the network address control.

## -see-also

<a href="/windows/desktop/api/shellapi/nf-shellapi-netaddr_setallowtype">NetAddr_SetAllowType</a>
