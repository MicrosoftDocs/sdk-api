---
UID: NF:ws2spi.WSCInstallQOSTemplate
title: WSCInstallQOSTemplate function (ws2spi.h)
description: Installs the specified QoS template in the system configuration database.
helpviewer_keywords: ["WSCInstallQOSTemplate","WSCInstallQOSTemplate function [Winsock]","winsock.wscinstallqostemplate","ws2spi/WSCInstallQOSTemplate"]
old-location: winsock\wscinstallqostemplate.htm
tech.root: WinSock
ms.assetid: b83cfb67-c3be-49aa-930d-d6b056f7bde2
ms.date: 12/05/2018
ms.keywords: WSCInstallQOSTemplate, WSCInstallQOSTemplate function [Winsock], winsock.wscinstallqostemplate, ws2spi/WSCInstallQOSTemplate
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
 - WSCInstallQOSTemplate
 - ws2spi/WSCInstallQOSTemplate
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
 - WSCInstallQOSTemplate
---

# WSCInstallQOSTemplate function


## -description

<p class="CCE_Message">[ This function is not supported in Windows Vista and subsequent versions of the operating system.]

The 
**WSCInstallQOSTemplate** function installs the specified QoS template in the system configuration database.

## -parameters

### -param Guid [in]

The globally unique identifier (GUID) for the quality of service (QoS) provider.

### -param QosName [in]

A pointer to a <a href="/windows/desktop/api/ws2def/ns-ws2def-wsabuf">WSABUF</a> structure that contains the  QoS name of the template to install.

### -param Qos [in]

A pointer to a <a href="/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a> structure that specifies the quality of service flow specifications and any provider-specific information for the QoS template.

## -returns

If 
**WSCInstallQOSTemplate** function  succeeds, the return value is zero. Otherwise, it returns one of the following error codes.

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
One or more of the arguments are invalid. This error is returned if the QoS provider specified in the <i>Guid</i> parameter is invalid or the QoS template name specified in the <i>QosName</i> parameter is invalid. This error is also returned if the contents of the template structure specified in the <i>Qos</i> parameter is invalid or incomplete.

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

## -remarks

The **WSCInstallQOSTemplate** function is not supported on Windows Vista and later. If this function is called on Windows Vista, and error is returned.

The **WSCInstallQOSTemplate** function installs a QoS template, based on a QoS name. The caller of the **WSCInstallQOSTemplate** function must have appropriate administrative rights for the call to succeed.
 

The <a href="/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a> structure that contains the QoS settings can later be retrieved by calling the <a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpwspgetqosbyname">WSPGetQOSByName</a> function and passing in the associated QoS name. 

The 
**WSCInstallQOSTemplate** function installs a named QoS template that contains the  
<a href="/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a> structure specified in the <i>Qos</i> parameter. If a QoS template already exists with the QoS name specified in the <i>Qosname</i> parameter, the settings specified in the <i>Qos</i> parameter replace the settings of the existing template. 

If the <i>Guid</i> parameter is set to **NULL**, the installed QOS template applies to all service providers. If the <i>Guid</i> parameter is not **NULL**, then the installed QoS template applies only to the provider indicated by the <i>Guid</i> parameter.

QoS template settings are stored in nonvolatile storage, so subsequent calls to 
the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetqosbyname">WSAGetQOSByName</a> function with the same QoS name specified in the <i>lpQOSName</i> parameter, return the 
same **QOS** structure passed to the **WSCInstallQOSTemplate** function . 

Windows Sockets 2 includes a base set of QoS templates. You can override and replace any of these QoS templates or change an existing QoS template by simply installing a new template with the existing name. You do not need to delete an existing template before replacing or modifying it. You cannot delete the base set of QoS-named templates included in Windows Sockets 2. However, you can delete templates added subsequently, perhaps by other service providers.

The <i>Qos</i> parameter points to a 
**QOS** structure that can include a 
buffer that contains provider-specific settings in the  **ProviderSpecific** member of the **QOS** structure. Any provider-specific settings are stored with the basic 
 **QOS** structure and are returned in subsequent 
calls to the **WSAGetQOSByName** function.

The **ProviderSpecific** member of the **QOS** structure can be set even if the <i>Guid</i> parameter is set to **NULL** to install a global QoS template for all service providers.  Note that this practice may lead a service provider to ignore the **ProviderSpecific** member of the **QOS** structure if the service provider does not recognize its contents. The recommended use of 
**WSCInstallQOSTemplate** function is to include provider-specific settings in the **ProviderSpecific** member of the **QOS** structure only if the named template is being installed on a particular service provider (the <i>Guid</i> parameter is not **NULL**).

## -see-also

<a href="/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-wsabuf">WSABUF</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpwspgetqosbyname">WSPGetQOSByName</a>

