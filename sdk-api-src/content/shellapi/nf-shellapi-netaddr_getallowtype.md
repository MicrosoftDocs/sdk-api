---
UID: NF:shellapi.NetAddr_GetAllowType
title: NetAddr_GetAllowType macro
author: windows-sdk-content
description: Retrieves the network address types that a specified network address control accepts.
old-location: shell\NetAddr_GetAllowType.htm
tech.root: shell
ms.assetid: 21533513-86c2-418b-ab62-3c1b2db9bc2f
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: NetAddr_GetAllowType, NetAddr_GetAllowType macro [Windows Shell], _shell_NetAddr_GetAllowType, shell.NetAddr_GetAllowType, shellapi/NetAddr_GetAllowType
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
 - NetAddr_GetAllowType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetAddr_GetAllowType macro


## -description


Retrieves the network address types that a specified network address control accepts.


## -parameters




### -param hwnd [in]

A handle to the network address control.


## -remarks



The returned mask is the criterion used to validate a network address in the macro <a href="https://msdn.microsoft.com/2d0310a8-89ca-41b5-8afc-faec29bd23ba">NetAddr_GetAddress</a>.

Use this macro for a network address control only. To instantiate, use the class <b>msctls_netaddress</b> defined in Shellapi.h. Call <a href="https://msdn.microsoft.com/52b475e3-7335-4c34-80d7-ccd81af0e0ec">InitNetworkAddressControl</a> at run time before calling this macro. This initializes the common controls library that contains the network address control.




## -see-also




<a href="https://msdn.microsoft.com/2fa97abd-79c8-41ce-bd0e-75941bf4d005">NetAddr_SetAllowType</a>
 

 

