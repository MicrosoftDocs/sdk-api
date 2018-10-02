---
UID: NF:shellapi.NetAddr_SetAllowType
title: NetAddr_SetAllowType macro
author: windows-sdk-content
description: Sets the network address types that a specified network address control accepts.
old-location: shell\NetAddr_SetAllowType.htm
tech.root: Shell
ms.assetid: 2fa97abd-79c8-41ce-bd0e-75941bf4d005
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: NetAddr_SetAllowType, NetAddr_SetAllowType macro [Windows Shell], _shell_NetAddr_SetAllowType, shell.NetAddr_SetAllowType, shellapi/NetAddr_SetAllowType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetAddr_SetAllowType macro


## -description


Sets the network address types that a specified network address control accepts.


## -parameters




### -param hwnd [in]

A handle to the network address control.


### -param addrMask [in]

Specifies the network address types as one or more of the <a href="https://msdn.microsoft.com/4144dac9-772c-49cb-b924-e852fb4c81c7">NET_STRING</a> constants.
                


## -remarks



The mask set is the criterion used to validate a network address in the macro <a href="https://msdn.microsoft.com/2d0310a8-89ca-41b5-8afc-faec29bd23ba">NetAddr_GetAddress</a>.

Use this macro for a network address control only. To instantiate, use the class <b>msctls_netaddress</b> defined in Shellapi.h. Call <a href="https://msdn.microsoft.com/52b475e3-7335-4c34-80d7-ccd81af0e0ec">InitNetworkAddressControl</a> at run time before calling this macro. This initializes the common controls library that contains the network address control.




## -see-also




<a href="https://msdn.microsoft.com/21533513-86c2-418b-ab62-3c1b2db9bc2f">NetAddr_GetAllowType</a>
 

 

