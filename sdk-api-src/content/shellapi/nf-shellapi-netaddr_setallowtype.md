---
UID: NF:shellapi.NetAddr_SetAllowType
title: NetAddr_SetAllowType macro (shellapi.h)
description: Sets the network address types that a specified network address control accepts.
helpviewer_keywords: ["NetAddr_SetAllowType","NetAddr_SetAllowType macro [Windows Shell]","_shell_NetAddr_SetAllowType","shell.NetAddr_SetAllowType","shellapi/NetAddr_SetAllowType"]
old-location: shell\NetAddr_SetAllowType.htm
tech.root: shell
ms.assetid: 2fa97abd-79c8-41ce-bd0e-75941bf4d005
ms.date: 12/05/2018
ms.keywords: NetAddr_SetAllowType, NetAddr_SetAllowType macro [Windows Shell], _shell_NetAddr_SetAllowType, shell.NetAddr_SetAllowType, shellapi/NetAddr_SetAllowType
f1_keywords:
- shellapi/NetAddr_SetAllowType
dev_langs:
- c++
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
- NetAddr_SetAllowType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NetAddr_SetAllowType macro


## -description


Sets the network address types that a specified network address control accepts.


## -parameters




### -param hwnd [in]

A handle to the network address control.


### -param addrMask [in]

Specifies the network address types as one or more of the <a href="https://docs.microsoft.com/windows/desktop/shell/net-string">NET_STRING</a> constants.
                


## -remarks



The mask set is the criterion used to validate a network address in the macro <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-netaddr_getaddress">NetAddr_GetAddress</a>.

Use this macro for a network address control only. To instantiate, use the class <b>msctls_netaddress</b> defined in Shellapi.h. Call <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-initnetworkaddresscontrol">InitNetworkAddressControl</a> at run time before calling this macro. This initializes the common controls library that contains the network address control.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-netaddr_getallowtype">NetAddr_GetAllowType</a>
 

 

