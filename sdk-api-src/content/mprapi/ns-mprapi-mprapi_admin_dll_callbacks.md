---
UID: NS:mprapi._MPRAPI_ADMIN_DLL_CALLBACKS
title: MPRAPI_ADMIN_DLL_CALLBACKS (mprapi.h)
description: The MPRAPI_ADMIN_DLL_CALLBACKS structure is used by the MprAdminInitializeDllEx function to register the callback function pointers.
helpviewer_keywords: ["*PMPRAPI_ADMIN_DLL_CALLBACKS","MPRAPI_ADMIN_DLL_CALLBACKS","MPRAPI_ADMIN_DLL_CALLBACKS structure [RAS]","MPRAPI_ADMIN_DLL_VERSION_1","MPRAPI_ADMIN_DLL_VERSION_2","PMPRAPI_ADMIN_DLL_CALLBACKS","PMPRAPI_ADMIN_DLL_CALLBACKS structure pointer [RAS]","mprapi/MPRAPI_ADMIN_DLL_CALLBACKS","mprapi/PMPRAPI_ADMIN_DLL_CALLBACKS","rras.mprapi_admin_dll_callbacks"]
old-location: rras\mprapi_admin_dll_callbacks.htm
tech.root: RRAS
ms.assetid: b36036e3-1aee-41e6-b777-98455b04e44b
ms.date: 12/05/2018
ms.keywords: '*PMPRAPI_ADMIN_DLL_CALLBACKS, MPRAPI_ADMIN_DLL_CALLBACKS, MPRAPI_ADMIN_DLL_CALLBACKS structure [RAS], MPRAPI_ADMIN_DLL_VERSION_1, MPRAPI_ADMIN_DLL_VERSION_2, PMPRAPI_ADMIN_DLL_CALLBACKS, PMPRAPI_ADMIN_DLL_CALLBACKS structure pointer [RAS], mprapi/MPRAPI_ADMIN_DLL_CALLBACKS, mprapi/PMPRAPI_ADMIN_DLL_CALLBACKS, rras.mprapi_admin_dll_callbacks'
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: MPRAPI_ADMIN_DLL_CALLBACKS, *PMPRAPI_ADMIN_DLL_CALLBACKS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MPRAPI_ADMIN_DLL_CALLBACKS
 - mprapi/_MPRAPI_ADMIN_DLL_CALLBACKS
 - PMPRAPI_ADMIN_DLL_CALLBACKS
 - mprapi/PMPRAPI_ADMIN_DLL_CALLBACKS
 - MPRAPI_ADMIN_DLL_CALLBACKS
 - mprapi/MPRAPI_ADMIN_DLL_CALLBACKS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - MPRAPI_ADMIN_DLL_CALLBACKS
---

# MPRAPI_ADMIN_DLL_CALLBACKS structure


## -description

The 
<b>MPRAPI_ADMIN_DLL_CALLBACKS</b> structure is used by the 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininitializedllex">MprAdminInitializeDllEx</a> function to register the  callback function pointers.

## -struct-fields

### -field revision

A value that represents the version of this structure.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_ADMIN_DLL_VERSION_1"></a><a id="mprapi_admin_dll_version_1"></a><dl>
<dt><b>MPRAPI_ADMIN_DLL_VERSION_1</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_ex">RAS_CONNECTION_EX</a> structure and the callback function pointers that use it as a parameter are not supported by this structure.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_ADMIN_DLL_VERSION_2"></a><a id="mprapi_admin_dll_version_2"></a><dl>
<dt><b>MPRAPI_ADMIN_DLL_VERSION_2</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_ex">RAS_CONNECTION_EX</a> structure and the callback function pointers that use it as a parameter are supported by this structure.

</td>
</tr>
</table>

### -field lpfnMprAdminGetIpAddressForUser

A function pointer to an instance of the <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmingetipaddressforuser">MprAdminGetIpAddressForUser</a> callback. The callback prototype is defined as:


```cpp
typedef DWORD (APIENTRY * PMPRADMINGETIPADDRESSFORUSER)(WCHAR *, WCHAR *, DWORD *, BOOL *);

```

### -field lpfnMprAdminReleaseIpAddress

A function pointer to an instance of the <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminreleaseipaddress">MprAdminReleaseIpAddress</a> callback. The callback prototype is defined as:


```cpp
typedef VOID  (APIENTRY * PMPRADMINRELEASEIPADRESS)(WCHAR *, WCHAR *, DWORD *);

```

### -field lpfnMprAdminGetIpv6AddressForUser

A function pointer to an instance of the <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmingetipv6addressforuser">MprAdminGetIpv6AddressForUser</a> callback. The callback prototype is defined as:


```cpp
typedef DWORD (APIENTRY * PMPRADMINGETIPV6ADDRESSFORUSER)(WCHAR *, WCHAR *, IN6_ADDR *, BOOL *);

```

### -field lpfnMprAdminReleaseIpV6AddressForUser

A function pointer to an instance of the <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminreleaseipv6addressforuser">MprAdminReleaseIpv6AddressForUser</a> callback. The callback prototype is defined as:


```cpp
typedef VOID  (APIENTRY * PMPRADMINRELEASEIPV6ADDRESSFORUSER)(WCHAR *, WCHAR *, IN6_ADDR *);

```

### -field lpfnRasAdminAcceptNewLink

A function pointer to an instance of the <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewlink">MprAdminAcceptNewLink</a> callback. The callback prototype is defined as:


```cpp
typedef BOOL  (APIENTRY * PMPRADMINACCEPTNEWLINK)(RAS_PORT_0 *, RAS_PORT_1 *);

```

### -field lpfnRasAdminLinkHangupNotification

A function pointer to an instance of the <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminlinkhangupnotification">MprAdminLinkHangupNotification</a> callback. The callback prototype is defined as:


```cpp
typedef VOID  (APIENTRY * PMPRADMINLINKHANGUPNOTIFICATION)(RAS_PORT_0 *, RAS_PORT_1 *);

```

### -field lpfnRasAdminTerminateDll

A function pointer to an instance of the <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminterminatedll">MprAdminTerminateDll</a> callback. The callback prototype is defined as:


```cpp
typedef DWORD (APIENTRY * PMPRADMINTERMINATEDLL)();

```

### -field lpfnRasAdminAcceptNewConnectionEx

A function pointer to an instance of the <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewconnectionex">MprAdminAcceptNewConnectionEx</a>  callback. The callback prototype is defined as:


```cpp
typedef BOOL  (APIENTRY * PMPRADMINACCEPTNEWCONNECTIONEX)(RAS_CONNECTION_EX *);

```

### -field lpfnRasAdminAcceptEndpointChangeEx

### -field lpfnRasAdminAcceptReauthenticationEx

A function pointer to an instance of the <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptreauthenticationex">MprAdminAcceptReauthenticationEx</a> callback. The callback prototype is defined as:


```cpp
typedef BOOL  (APIENTRY * PMPRADMINACCEPTREAUTHENTICATIONEX)(RAS_CONNECTION_EX *);

```

### -field lpfnRasAdminConnectionHangupNotificationEx

A function pointer to an instance of the <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotificationex">MprAdminConnectionHangupNotificationEx</a> callback. The callback prototype is defined as:


```cpp
typedef VOID  (APIENTRY * PMPRADMINCONNECTIONHANGUPNOTIFICATIONEX)(RAS_CONNECTION_EX *);

```

### -field lpfnRASValidatePreAuthenticatedConnectionEx

## -remarks

The following restrictions apply to the callback functions in the <b>MPRAPI_ADMIN_DLL_CALLBACKS</b> structure:

<ul>
<li>Both <b>lpfnMprAdminGetIpv6AddressForUser</b> and <b>lpfnMprAdminReleaseIpV6AddressForUser</b> must be implemented, or neither are implemented.</li>
<li>Both <b>lpfnMprAdminGetIpAddressForUser</b> and <b>lpfnMprAdminReleaseIpAddress</b> must be implemented, or neither are implemented.</li>
<li>Either <b>lpfnRasAdminLinkHangupNotification</b> or <b>lpfnRasAdminAcceptNewLink</b> must be implemented.</li>
<li>Either <b>lpfnRasAdminAcceptNewConnectionEx</b> or <b>lpfnRasAdminConnectionHangupNotificationEx</b> must be implemented.</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)">IN6_ADDR</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewconnectionex">MprAdminAcceptNewConnectionEx</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewlink">MprAdminAcceptNewLink</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptreauthenticationex">MprAdminAcceptReauthenticationEx</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotificationex">MprAdminConnectionHangupNotificationEx</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmingetipaddressforuser">MprAdminGetIpAddressForUser</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmingetipv6addressforuser">MprAdminGetIpv6AddressForUser</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininitializedll">MprAdminInitializeDll</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminlinkhangupnotification">MprAdminLinkHangupNotification</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminreleaseipaddress">MprAdminReleaseIpAddress</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminreleaseipv6addressforuser">MprAdminReleaseIpv6AddressForUser</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminterminatedll">MprAdminTerminateDll</a>



<a href="/windows/desktop/RRAS/ras-administration-structures">RAS Administration Structures</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_ex">RAS_CONNECTION_EX</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_port_0">RAS_PORT_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_port_1">RAS_PORT_1</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>