---
UID: NF:shellapi.NetAddr_GetAddress
title: NetAddr_GetAddress macro (shellapi.h)
description: Indicates whether a network address conforms to a specified type and format.
helpviewer_keywords: ["NetAddr_GetAddress","NetAddr_GetAddress macro [Windows Shell]","_shell_NetAddr_GetAddress","shell.NetAddr_GetAddress","shellapi/NetAddr_GetAddress"]
old-location: shell\NetAddr_GetAddress.htm
tech.root: shell
ms.assetid: 2d0310a8-89ca-41b5-8afc-faec29bd23ba
ms.date: 07/01/2025
ms.keywords: NetAddr_GetAddress, NetAddr_GetAddress macro [Windows Shell], _shell_NetAddr_GetAddress, shell.NetAddr_GetAddress, shellapi/NetAddr_GetAddress
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
 - NetAddr_GetAddress
 - shellapi/NetAddr_GetAddress
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
 - NetAddr_GetAddress
---

# NetAddr_GetAddress macro

## -syntax

```cpp
HRESULT NetAddr_GetAddress(
             HWND hwnd,
  [in, out]  LPARAM pv
);
```

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

Returns one of the following values of type **HRESULT**:

- **E_INVALIDARG** - The calling application failed to allocate a **NC_ADDRESS** structure.
- **ERROR_INSUFFICIENT_BUFFER** - The out buffer is too small to hold the parsed network address.
- **ERROR_INVALID_PARAMETER** - The network address string is not of any type specified.
- **ERROR_SUCCESS** - The operation was successful.
- **S_FALSE** - There is no address in the network address control to validate.


## -description

Indicates whether a network address conforms to a specified type and format.

## -parameters

### -param hwnd

A handle to the network address control that contains the address to validate.

### -param pv [in, out]

A pointer to an <a href="/windows/desktop/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> structure to receive network address information in parsed form, if the address format and type in the control specified by <i>hwnd</i> are validated. The calling application is responsible for allocating the memory for this structure.

## -remarks

Use the <b>NetAddr_GetAddress</b> macro to validate a network address in a network address control against a preset network address type mask. To instantiate, use the class <b>msctls_netaddress</b> defined in Shellapi.h. Call <a href="/windows/desktop/api/shellapi/nf-shellapi-initnetworkaddresscontrol">InitNetworkAddressControl</a> at run time before calling this macro. This initializes the common controls library that contains the network address control.

This macro gets the network address string from a network address control, parses the string, and checks whether the string matches a network address type mask. If the string matches the mask, the function returns S_OK and returns the string in parsed form to the calling application (including the port number, prefix length, and other address information), using the <a href="/windows/desktop/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> structure pointed to by <i>pv</i>. This macro returns E_INVALIDARG if the calling application fails to allocate the structure pointed to by <i>pv</i>.

Representations of Internet Protocol (IP) address versions 4 and 6 (v4/v6) for services and networks, as well as named Internet addresses and services using Domain Name System (DNS) format are parsed. If the network address string represents a named host name (DNS) or service, the value returned in the <b>PrefixLength</b> member of <a href="/windows/desktop/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> is zero.

Set the network address type mask using the <a href="/windows/desktop/api/shellapi/nf-shellapi-netaddr_setallowtype">NetAddr_SetAllowType</a> macro before you call the <b>NetAddr_GetAddress</b> macro.

## -see-also

<a href="/windows/desktop/api/shellapi/nf-shellapi-netaddr_getallowtype">NetAddr_GetAllowType</a>
