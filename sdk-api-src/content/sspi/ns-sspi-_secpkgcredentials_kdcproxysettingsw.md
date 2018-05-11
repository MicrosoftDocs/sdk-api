---
UID: NS:sspi._SecPkgCredentials_KdcProxySettingsW
title: "_SecPkgCredentials_KdcProxySettingsW"
author: windows-driver-content
description: Specifies the Kerberos proxy settings for the credentials.
old-location: security\secpkgcredentials_kdcproxysettings.htm
old-project: SecAuthN
ms.assetid: 42BC75B8-6392-4FD4-95BC-266B3AFDDC62
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*PSecPkgCredentials_KdcProxySettingsW, PSecPkgCredentials_KdcProxySettings, PSecPkgCredentials_KdcProxySettings structure pointer [Security], SecPkgCredentials_KdcProxySettings, SecPkgCredentials_KdcProxySettings structure [Security], SecPkgCredentials_KdcProxySettingsW, _SecPkgCredentials_KdcProxySettingsW, security.secpkgcredentials_kdcproxysettings, sspi/PSecPkgCredentials_KdcProxySettings, sspi/SecPkgCredentials_KdcProxySettings, sspi/SecPkgCredentials_KdcProxySettingsW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: sspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SecPkgCredentials_KdcProxySettingsW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SecPkgCredentials_KdcProxySettingsW, *PSecPkgCredentials_KdcProxySettingsW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Sspi.h
api_name:
-	SecPkgCredentials_KdcProxySettings
-	SecPkgCredentials_KdcProxySettingsW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# _SecPkgCredentials_KdcProxySettingsW structure


## -description


Specifies the Kerberos proxy settings for the credentials.


## -struct-fields




### -field Version

Version for the Kerberos proxy settings where KDC_PROXY_SETTINGS_V1 is defined as 1.


### -field Flags

Flags for the Kerberos proxy settings.


### -field ProxyServerOffset

The offset of the proxy server. This member is optional.


### -field ProxyServerLength

Length of the proxy server.


### -field ClientTlsCredOffset

The offset of the client credentials. This member is optional.


### -field ClientTlsCredLength

Length of the client credentials.

