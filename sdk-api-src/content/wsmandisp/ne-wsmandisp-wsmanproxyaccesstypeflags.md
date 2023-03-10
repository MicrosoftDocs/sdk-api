---
UID: NE:wsmandisp._WSManProxyAccessTypeFlags
title: WSManProxyAccessTypeFlags (wsmandisp.h)
description: Defines the proxy access type flags.
helpviewer_keywords: ["WSManProxyAccessTypeFlags","WSManProxyAccessTypeFlags enumeration [Windows Remote Management]","WSManProxyAutoDetect","WSManProxyIEConfig","WSManProxyNoProxyServer","WSManProxyWinHttpConfig","winrm.wsmanproxyaccesstypeflags","wsmandisp/WSManProxyAccessTypeFlags","wsmandisp/WSManProxyAutoDetect","wsmandisp/WSManProxyIEConfig","wsmandisp/WSManProxyNoProxyServer","wsmandisp/WSManProxyWinHttpConfig"]
old-location: winrm\wsmanproxyaccesstypeflags.htm
tech.root: winrm
ms.assetid: c17c3600-6a19-4937-90ff-1a4f7cf5b123
ms.date: 12/05/2018
ms.keywords: WSManProxyAccessTypeFlags, WSManProxyAccessTypeFlags enumeration [Windows Remote Management], WSManProxyAutoDetect, WSManProxyIEConfig, WSManProxyNoProxyServer, WSManProxyWinHttpConfig, winrm.wsmanproxyaccesstypeflags, wsmandisp/WSManProxyAccessTypeFlags, wsmandisp/WSManProxyAutoDetect, wsmandisp/WSManProxyIEConfig, wsmandisp/WSManProxyNoProxyServer, wsmandisp/WSManProxyWinHttpConfig
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WSManProxyAccessTypeFlags
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - _WSManProxyAccessTypeFlags
 - wsmandisp/_WSManProxyAccessTypeFlags
 - WSManProxyAccessTypeFlags
 - wsmandisp/WSManProxyAccessTypeFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WSManDisp.h
api_name:
 - WSManProxyAccessTypeFlags
---

# WSManProxyAccessTypeFlags enumeration


## -description

Defines the proxy access type flags.

## -enum-fields

### -field WSManProxyIEConfig:0x1

Use the Internet Explorer proxy configuration for the current user.

### -field WSManProxyWinHttpConfig:0x2

Use the proxy settings configured for WinHTTP. This is the default setting.

### -field WSManProxyAutoDetect:0x4

Force autodetection of a proxy.

### -field WSManProxyNoProxyServer:0x8

Do not use a proxy server. All host names are resolved locally.

