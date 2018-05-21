---
UID: NS:wtsapi32._WTSCLIENTW
title: "_WTSCLIENTW"
author: windows-driver-content
description: Contains information about a Remote Desktop Connection (RDC) client.
old-location: termserv\wtsclient.htm
old-project: TermServ
ms.assetid: 864b7560-3f19-4a73-a02b-b82caa88b2de
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: "*PWTSCLIENTW, PWTSCLIENT, PWTSCLIENT structure pointer [Remote Desktop Services], WTSCLIENT, WTSCLIENT structure [Remote Desktop Services], WTSCLIENTA, WTSCLIENTW, _WTSCLIENTW, termserv.wtsclient, wtsapi32/PWTSCLIENT, wtsapi32/WTSCLIENT, wtsapi32/WTSCLIENTA, wtsapi32/WTSCLIENTW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSCLIENTW (Unicode) and WTSCLIENTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WTSCLIENTW, *PWTSCLIENTW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wtsapi32.h
api_name:
-	WTSCLIENT
-	WTSCLIENTA
-	WTSCLIENTW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WTSCLIENTW structure


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



