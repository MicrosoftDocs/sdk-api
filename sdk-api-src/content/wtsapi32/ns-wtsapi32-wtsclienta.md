---
UID: NS:wtsapi32._WTSCLIENTA
title: WTSCLIENTA (wtsapi32.h)
description: Contains information about a Remote Desktop Connection (RDC) client. (ANSI)
helpviewer_keywords: ["*PWTSCLIENTA","PWTSCLIENT","PWTSCLIENT structure pointer [Remote Desktop Services]","WTSCLIENT","WTSCLIENT structure [Remote Desktop Services]","WTSCLIENTA","WTSCLIENTW","termserv.wtsclient","wtsapi32/PWTSCLIENT","wtsapi32/WTSCLIENT","wtsapi32/WTSCLIENTA","wtsapi32/WTSCLIENTW"]
old-location: termserv\wtsclient.htm
tech.root: TermServ
ms.assetid: 864b7560-3f19-4a73-a02b-b82caa88b2de
ms.date: 12/05/2018
ms.keywords: '*PWTSCLIENTA, PWTSCLIENT, PWTSCLIENT structure pointer [Remote Desktop Services], WTSCLIENT, WTSCLIENT structure [Remote Desktop Services], WTSCLIENTA, WTSCLIENTW, termserv.wtsclient, wtsapi32/PWTSCLIENT, wtsapi32/WTSCLIENT, wtsapi32/WTSCLIENTA, wtsapi32/WTSCLIENTW'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WTSCLIENTA, *PWTSCLIENTA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTSCLIENTA
 - wtsapi32/_WTSCLIENTA
 - PWTSCLIENTA
 - wtsapi32/PWTSCLIENTA
 - WTSCLIENTA
 - wtsapi32/WTSCLIENTA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsapi32.h
api_name:
 - WTSCLIENT
 - WTSCLIENTA
 - WTSCLIENTW
---

# WTSCLIENTA structure


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
      member of the <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_client_display">WTS_CLIENT_DISPLAY</a> 
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




> [!NOTE]
> The wtsapi32.h header defines WTSCLIENT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
