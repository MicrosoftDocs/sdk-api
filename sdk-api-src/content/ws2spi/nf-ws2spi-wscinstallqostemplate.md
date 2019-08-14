---
UID: NF:ws2spi.WSCInstallQOSTemplate
title: WSCInstallQOSTemplate function (ws2spi.h)
author: windows-sdk-content
description: Installs the specified QoS template in the system configuration database.
old-location: winsock\wscinstallqostemplate.htm
tech.root: WinSock
ms.assetid: b83cfb67-c3be-49aa-930d-d6b056f7bde2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WSCInstallQOSTemplate, WSCInstallQOSTemplate function [Winsock], winsock.wscinstallqostemplate, ws2spi/WSCInstallQOSTemplate
ms.topic: function
f1_keywords: 
 - "ws2spi/WSCInstallQOSTemplate"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2spi.h
api_name:
 - WSCInstallQOSTemplate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WSCInstallQOSTemplate function


## -description


<p class="CCE_Message">[ This function is not supported in Windows Vista and subsequent versions of the operating system.]

The 
<b>WSCInstallQOSTemplate</b> function installs the specified QoS template in the system configuration database.


## -parameters




### -param Guid [in]

The globally unique identifier (GUID) for the quality of service (QoS) provider.


### -param QosName [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/ws2def/ns-ws2def-wsabuf">WSABUF</a> structure that contains the  QoS name of the template to install.


### -param Qos [in]

A pointer to a <a href="https://docs.microsoft.com/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a> structure that specifies the quality of service flow specifications and any provider-specific information for the QoS template.


## -returns



If 
<b>WSCInstallQOSTemplate</b> function  succeeds, the return value is zero. Otherwise, it returns one of the following error codes.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not in a valid part of the user address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments are invalid. This error is returned if the QoS provider specified in the <i>Guid</i> parameter is invalid or the QoS template name specified in the <i>QosName</i> parameter is invalid. This error is also returned if the contents of the template structure specified in the <i>Qos</i> parameter is invalid or incomplete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
 Memory cannot be allocated for buffers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a></b></dt>
</dl>
</td>
<td width="60%">
A nonrecoverable error occurred. This error is returned under several conditions including the following: the provider is already installed, the user lacks the administrative privileges required to write to the  Winsock registry, or a failure occurred when creating or installing a catalog entry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSASYSCALLFAILURE</a></b></dt>
</dl>
</td>
<td width="60%">
 A system call that should never fail has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
 Insufficient memory was available. This error is returned when there is insufficient memory to allocate a new catalog entry.

</td>
</tr>
</table>
 




## -remarks



The <b>WSCInstallQOSTemplate</b> function is not supported on Windows Vista and later. If this function is called on Windows Vista, and error is returned.

The <b>WSCInstallQOSTemplate</b> function installs a QoS template, based on a QoS name. The caller of the <b>WSCInstallQOSTemplate</b> function must have appropriate administrative rights for the call to succeed.
 

The <a href="https://docs.microsoft.com/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a> structure that contains the QoS settings can later be retrieved by calling the <a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspgetqosbyname">WSPGetQOSByName</a> function and passing in the associated QoS name. 

The 
<b>WSCInstallQOSTemplate</b> function installs a named QoS template that contains the  
<a href="https://docs.microsoft.com/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a> structure specified in the <i>Qos</i> parameter. If a QoS template already exists with the QoS name specified in the <i>Qosname</i> parameter, the settings specified in the <i>Qos</i> parameter replace the settings of the existing template. 

If the <i>Guid</i> parameter is set to <b>NULL</b>, the installed QOS template applies to all service providers. If the <i>Guid</i> parameter is not <b>NULL</b>, then the installed QoS template applies only to the provider indicated by the <i>Guid</i> parameter.

QoS template settings are stored in nonvolatile storage, so subsequent calls to 
the <a href="https://docs.microsoft.com/windows/desktop/api/winsock2/nf-winsock2-wsagetqosbyname">WSAGetQOSByName</a> function with the same QoS name specified in the <i>lpQOSName</i> parameter, return the 
same <b>QOS</b> structure passed to the <b>WSCInstallQOSTemplate</b> function . 

Windows Sockets 2 includes a base set of QoS templates. You can override and replace any of these QoS templates or change an existing QoS template by simply installing a new template with the existing name. You do not need to delete an existing template before replacing or modifying it. You cannot delete the base set of QoS-named templates included in Windows Sockets 2. However, you can delete templates added subsequently, perhaps by other service providers.

The <i>Qos</i> parameter points to a 
<b>QOS</b> structure that can include a 
buffer that contains provider-specific settings in the  <b>ProviderSpecific</b> member of the <b>QOS</b> structure. Any provider-specific settings are stored with the basic 
 <b>QOS</b> structure structure and are returned in subsequent 
calls to the <b>WSAGetQOSByName</b> function.

The <b>ProviderSpecific</b> member of the <b>QOS</b> structure can be set even if the <i>Guid</i> parameter is set to <b>NULL</b> to install a global QoS template for all service providers.  Note that this practice may lead a service provider to ignore the <b>ProviderSpecific</b> member of the <b>QOS</b> structure if the service provider does not recognize its contents. The recommended use of 
<b>WSCInstallQOSTemplate</b> function is to include provider-specific settings in the <b>ProviderSpecific</b> member of the <b>QOS</b> structure only if the named template is being installed on a particular service provider (the <i>Guid</i> parameter is not <b>NULL</b>).




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2def/ns-ws2def-wsabuf">WSABUF</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspgetqosbyname">WSPGetQOSByName</a>
 

 

