---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _WTSCLIENTA structure


## -description


Contains information about a Remote Desktop Connection (RDC) client.


## -struct-fields




### -field ClientName

The NetBIOS name of the client computer.


### -field Domain

The domain name of the client computer.


### -field UserName

The client user name.


### -field WorkDirectory

The folder for the initial program.


### -field InitialProgram

The program to start on connection.


### -field EncryptionLevel

The security level of encryption.


### -field ClientAddressFamily

The address family. This member can be <b>AF_INET</b>, <b>AF_INET6</b>, <b>AF_IPX</b>, <b>AF_NETBIOS</b>, or <b>AF_UNSPEC</b>.


### -field ClientAddress

The client network address.


### -field HRes

Horizontal dimension, in pixels, of the client's display.


### -field VRes

Vertical dimension, in pixels, of the client's display.


### -field ColorDepth

Color depth of the client's display. For possible values, see the <b>ColorDepth</b> 
      member of the <a href="https://msdn.microsoft.com/0d5e0a9d-23b0-4302-ade3-eb9fbd7f787d">WTS_CLIENT_DISPLAY</a> 
      structure.


### -field ClientDirectory

The location of the client ActiveX control DLL.


### -field ClientBuildNumber

The client build number.


### -field ClientHardwareId

Reserved.


### -field ClientProductId

Reserved.


### -field OutBufCountHost

The number of output buffers on the server per session.


### -field OutBufCountClient

The number of output buffers on the client.


### -field OutBufLength

The length of the output buffers, in bytes.


### -field DeviceId

The device ID of the network adapter.


## -remarks



For the <b>ClientAddressFamily</b> member, <b>AF_INET</b>  (IPv4) will return in string format, for example "127.0.0.1". 
<b>AF_INET6</b> (IPv6) will return in binary form.



