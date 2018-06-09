---
UID: NF:shellapi.NetAddr_GetAddress
title: NetAddr_GetAddress macro
author: windows-sdk-content
description: Indicates whether a network address conforms to a specified type and format.
old-location: shell\NetAddr_GetAddress.htm
old-project: shell
ms.assetid: 2d0310a8-89ca-41b5-8afc-faec29bd23ba
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: NetAddr_GetAddress, NetAddr_GetAddress macro [Windows Shell], _shell_NetAddr_GetAddress, shell.NetAddr_GetAddress, shellapi/NetAddr_GetAddress
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SHSTOCKICONID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shellapi.h
api_name:
 - NetAddr_GetAddress
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# NetAddr_GetAddress macro


## -description


Indicates whether a network address conforms to a specified type and format.


## -parameters




### -param hwnd

A handle to the network address control that contains the address to validate.


### -param pv [in, out]

A pointer to an <a href="https://msdn.microsoft.com/1dfb0f6a-3aa5-486b-bbd0-8a24070bca19">NC_ADDRESS</a> structure to receive network address information in parsed form, if the address format and type in the control specified by <i>hwnd</i> are validated. The calling application is responsible for allocating the memory for this structure.


## -remarks



Use the <b>NetAddr_GetAddress</b> macro to validate a network address in a network address control against a preset network address type mask. To instantiate, use the class <b>msctls_netaddress</b> defined in Shellapi.h. Call <a href="https://msdn.microsoft.com/52b475e3-7335-4c34-80d7-ccd81af0e0ec">InitNetworkAddressControl</a> at run time before calling this macro. This initializes the common controls library that contains the network address control.

This macro gets the network address string from a network address control, parses the string, and checks whether the string matches a network address type mask. If the string matches the mask, the function returns S_OK and returns the string in parsed form to the calling application (including the port number, prefix length, and other address information), using the <a href="https://msdn.microsoft.com/1dfb0f6a-3aa5-486b-bbd0-8a24070bca19">NC_ADDRESS</a> structure pointed to by <i>pv</i>. This macro returns E_INVALIDARG if the calling application fails to allocate the structure pointed to by <i>pv</i>.

Representations of Internet Protocol (IP) address versions 4 and 6 (v4/v6) for services and networks, as well as named Internet addresses and services using Domain Name System (DNS) format are parsed. If the network address string represents a named host name (DNS) or service, the value returned in the <b>PrefixLength</b> member of <a href="https://msdn.microsoft.com/1dfb0f6a-3aa5-486b-bbd0-8a24070bca19">NC_ADDRESS</a> is zero.

Set the network address type mask using the <a href="https://msdn.microsoft.com/2fa97abd-79c8-41ce-bd0e-75941bf4d005">NetAddr_SetAllowType</a> macro before you call the <b>NetAddr_GetAddress</b> macro.




## -see-also




<a href="https://msdn.microsoft.com/21533513-86c2-418b-ab62-3c1b2db9bc2f">NetAddr_GetAllowType</a>
 

 

