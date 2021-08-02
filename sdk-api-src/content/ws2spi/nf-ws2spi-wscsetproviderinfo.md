---
UID: NF:ws2spi.WSCSetProviderInfo
title: WSCSetProviderInfo function (ws2spi.h)
description: Sets the data value for the specified information class for a layered service provider (LSP).
helpviewer_keywords: ["WSCSetProviderInfo","WSCSetProviderInfo function [Winsock]","winsock.wscsetproviderinfo","ws2spi/WSCSetProviderInfo"]
old-location: winsock\wscsetproviderinfo.htm
tech.root: WinSock
ms.assetid: 10eed3e6-d5a0-4ba4-964e-3d924a231afb
ms.date: 12/05/2018
ms.keywords: WSCSetProviderInfo, WSCSetProviderInfo function [Winsock], winsock.wscsetproviderinfo, ws2spi/WSCSetProviderInfo
req.header: ws2spi.h
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
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSCSetProviderInfo
 - ws2spi/WSCSetProviderInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSCSetProviderInfo
---

# WSCSetProviderInfo function


## -description

<div class="alert">**Note**  Layered Service Providers are deprecated. Starting with Windows 8 and Windows Server 2012, use <a href="/windows/desktop/FWP/windows-filtering-platform-start-page">Windows Filtering Platform</a>.</div><div> </div>The 
**WSCSetProviderInfo** function sets the data value for the specified information class  for a layered service provider (LSP).

## -parameters

### -param lpProviderId [in]

A pointer to a globally unique identifier (GUID)  for the provider.

### -param InfoType [in]

The information class to be set for this LSP protocol entry.

### -param Info [in]

A pointer to a buffer that contains the information class data to set for the LSP protocol entry.

### -param InfoSize [in]

The size, in bytes, of the buffer pointed to by the <i>Info</i> parameter.

### -param Flags [in]

The flags used to modify the behavior of the **WSCSetProviderInfo** function call.

### -param lpErrno [out]

A pointer to the error code if the function fails.

## -returns

If no error occurs, **WSCSetProviderInfo** returns **ERROR_SUCCESS** (zero). Otherwise, it returns **SOCKET_ERROR**, and a specific error code is returned in the <i>lpErrno</i> parameter.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CALL_NOT_IMPLEMENTED</b></dl>
</dl>
</td>
<td width="60%">
The call is not implemented. This error is returned if **ProviderInfoAudit** is specified in the <i>InfoType</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dl>
</dl>
</td>
<td width="60%">
One or more of the arguments is not in a valid part of the user address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
One or more of the arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a></b></dl>
</dl>
</td>
<td width="60%">
A nonrecoverable error occurred. This error is returned under several conditions including the following: the user lacks the administrative privileges required to write to the Winsock registry, or a failure occurred when opening a Winsock catalog entry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dl>
</dl>
</td>
<td width="60%">
 Insufficient memory was available. This error is returned when there is insufficient memory to allocate a new catalog entry.

</td>
</tr>
</table>

## -remarks

**WSCSetProviderInfo** is used to set the information class data for a layered service provider. When the <i>InfoType</i> parameter is set to **ProviderInfoLspCategories**, on success **WSCSetProviderInfo** sets appropriate LSP category flags implemented by the provider based on the value passed in the <i>Info</i> parameter. 

Winsock 2 accommodates layered protocols. A layered protocol is one that implements only higher level communications functions, while relying on an underlying transport stack for the actual exchange of data with a remote endpoint. An example of a layered protocol or layered service provider would be a security layer that adds protocol to the connection establishment process in order to perform authentication and to establish a mutually agreed upon encryption scheme.  Such a security protocol would generally require the services of an underlying reliable transport protocol such as TCP or SPX.  The term base protocol refers to a protocol such as TCP or SPX which is capable of performing data communications with a remote endpoint. The term layered protocol is used to describe a protocol that cannot stand alone.  A protocol chain would then be defined as one or more layered protocols strung together and anchored by a base protocol.
A base protocol has the **ChainLen** member of the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure set to  **BASE_PROTOCOL** which is defined to be 1. A layered protocol has the **ChainLen** member of the **WSAPROTOCOL_INFO** structure set to **LAYERED_PROTOCOL** which is defined to be zero. A protocol chain has the **ChainLen** member of the **WSAPROTOCOL_INFO** structure set to greater than 1.

During LSP initialization, the LSP must provide pointers to a number of Winsock SPI functions.  These functions will be called during normal processing by the layer directly above the LSP (either another LSP or Ws2_32.dll).  

An LSP that implements an installable file system (IFS) can  selectively choose to provide pointers to functions which are implemented by itself, or pass back the pointers provided by the layer directly below the LSP.  Non-IFS LSPs, because they provide their own handles, must implement all of the Winsock SPI functions.  This is because each SPI will require the LSP to map all of the socket handles it created to the socket handle of the lower provider (either another LSP or the base protocol).

However, all LSPs perform their specific work by doing extra processing on only a subset of the Winsock SPI functions.

It is possible to define LSP categories based upon the subset of SPI functions an LSP implements and the nature of the extra processing performed for each of those functions.

By classifying LSPs, as well as classifying applications which use Winsock sockets, it becomes possible to selectively determine if an LSP should be involved in a given process at runtime.

On Windows Vista and later, an LSP can be classified based on how it interacts with Windows Sockets calls and data. An LSP category is an identifiable group of behaviors on a subset of Winsock SPI functions.  For example, an HTTP content filter would be categorized as a data inspector (the **LSP_INSPECTOR** category). The **LSP_INSPECTOR** category will inspect, but not alter, parameters to data transfer SPI functions. An application can query for the category of an LSP and choose to not load the LSP based on the LSP category and the application's set of permitted LSP categories.

The following table lists categories into which an LSP can be classified.<table>
<tr>
<th>LSP Category</th>
<th>Description</th>
</tr>
<tr>
<td>**LSP_CRYPTO_COMPRESS**</td>
<td>The LSP is a cryptography or data compression provider.</td>
</tr>
<tr>
<td>**LSP_FIREWALL**</td>
<td>The LSP is a firewall provider.</td>
</tr>
<tr>
<td>**LSP_LOCAL_CACHE**</td>
<td>The LSP is a local cache provider.
</td>
</tr>
<tr>
<td>**LSP_INBOUND_MODIFY**</td>
<td>The LSP modifies inbound data.</td>
</tr>
<tr>
<td>**LSP_INSPECTOR**</td>
<td>The LSP inspects or filters data.
</td>
</tr>
<tr>
<td>**LSP_OUTBOUND_MODIFY**</td>
<td>The LSP modifies outbound data.</td>
</tr>
<tr>
<td>**LSP_PROXY**</td>
<td>The LSP acts as a proxy and redirects packets.</td>
</tr>
<tr>
<td>**LSP_REDIRECTOR**</td>
<td>The LSP is a network redirector.</td>
</tr>
<tr>
<td>**LSP_SYSTEM**</td>
<td>The LSP is acceptable for use in services and system processes.</td>
</tr>
</table>
 
An LSP may belong to more than one category.  For example, firewall/security LSP could belong to both the inspector (**LSP_INSPECTOR**) and firewall (**LSP_FIREWALL**) categories.

If an LSP does not have category set, it is considered to be in the All Other category. This LSP category will not be loaded in services or system processes (for example, lsass, winlogon, and many svchost processes).

The **WSCSetProviderInfo** function can only be called by a user logged on as a member of the Administrators group. If **WSCSetProviderInfo** is called by a user that is not a member of the Administrators group, the function call will fail and **WSANO_RECOVERY** is returned in the <i>lpErrno</i> parameter. 
 This function can also fail because of user account control (UAC). If an application  that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a **requestedExecutionLevel** set to **requireAdministrator**. If the application on Windows Vista or Windows Server 2008 lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.

<div class="alert">**Note**  The TDI feature is deprecated and will be removed in future versions of Microsoft
    Windows. Depending on how you use TDI, use either the Winsock Kernel (WSK) or Windows Filtering Platform
    (WFP). For more information about WFP and WSK, see 
    
<a href="/windows/win32/fwp/windows-filtering-platform-start-page">Windows Filtering Platform</a> and 
    
<a href="/windows-hardware/drivers/ddi/content/_netvista/">Winsock Kernel</a>. For a Windows Core Networking
    blog entry about WSK and TDI, see 
    
<a href="/archive/blogs/wndp/">Introduction to Winsock Kernel
    (WSK)</a>.
</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinSock/categorizing-layered-service-providers-and-applications">Categorizing Layered Service Providers and Applications</a>
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a>
<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscgetapplicationcategory">WSCGetApplicationCategory</a>
<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscgetproviderinfo">WSCGetProviderInfo</a>
<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscsetapplicationcategory">WSCSetApplicationCategory</a>
<a href="/windows/desktop/api/ws2spi/ne-ws2spi-wsc_provider_info_type">WSC_PROVIDER_INFO_TYPE</a>
