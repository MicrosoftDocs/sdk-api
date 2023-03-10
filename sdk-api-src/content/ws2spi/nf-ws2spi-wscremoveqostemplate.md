---
UID: NF:ws2spi.WSCRemoveQOSTemplate
title: WSCRemoveQOSTemplate function (ws2spi.h)
description: Removes the specified QoS template from the system configuration database.
helpviewer_keywords: ["WSCRemoveQOSTemplate","WSCRemoveQOSTemplate function [Winsock]","winsock.wscremoveqostemplate","ws2spi/WSCRemoveQOSTemplate"]
old-location: winsock\wscremoveqostemplate.htm
tech.root: WinSock
ms.assetid: e3cb8428-98d8-4bc3-926c-baa7cbf5d679
ms.date: 12/05/2018
ms.keywords: WSCRemoveQOSTemplate, WSCRemoveQOSTemplate function [Winsock], winsock.wscremoveqostemplate, ws2spi/WSCRemoveQOSTemplate
req.header: ws2spi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSCRemoveQOSTemplate
 - ws2spi/WSCRemoveQOSTemplate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2spi.h
api_name:
 - WSCRemoveQOSTemplate
---

# WSCRemoveQOSTemplate function


## -description

<p class="CCE_Message">[ This function is not supported in Windows Vista and subsequent versions of the operating system.]

The 
**WSCRemoveQOSTemplate** function removes the specified QoS template from the system configuration database.

## -parameters

### -param Guid [in]

The globally unique identifier (GUID) for the quality of service (QoS) provider.

### -param QosName [in]

A pointer to a <a href="/windows/desktop/api/ws2def/ns-ws2def-wsabuf">WSABUF</a> structure that contains the  QoS name of the template to remove.

## -returns

If 
**WSCRemoveQOSTemplate** function  succeeds, the return value is zero. Otherwise, it returns one of the following error codes.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
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
One or more of the arguments are invalid. This error is returned if the if QoS provider specified in the <i>Guid</i> parameter is invalid or the QoS template name specified in the <i>QosName</i> parameter is invalid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dl>
</dl>
</td>
<td width="60%">
 Memory cannot be allocated for buffers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a></b></dl>
</dl>
</td>
<td width="60%">
A nonrecoverable error occurred. This error is returned under several conditions including the following: the provider is already installed, the user lacks the administrative privileges required to write to the  Winsock registry, or a failure occurred when creating or installing a catalog entry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSASYSCALLFAILURE</a></b></dl>
</dl>
</td>
<td width="60%">
 A system call that should never fail has failed.

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

## -see-also

<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wscinstallqostemplate">WSCInstallQOSTemplate</a>

