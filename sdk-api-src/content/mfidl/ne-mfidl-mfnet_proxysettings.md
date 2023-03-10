---
UID: NE:mfidl._MFNET_PROXYSETTINGS
title: MFNET_PROXYSETTINGS (mfidl.h)
description: Specifies how the default proxy locator will specify the connection settings to a proxy server.
helpviewer_keywords: ["MFNET_PROXYSETTINGS","MFNET_PROXYSETTINGS enumeration [Media Foundation]","MFNET_PROXYSETTING_AUTO","MFNET_PROXYSETTING_BROWSER","MFNET_PROXYSETTING_MANUAL","MFNET_PROXYSETTING_NONE","b9ec76bc-d8d1-4ba1-b6c4-02bcac9b53a0","mf.mfnet_proxysettings","mfidl/MFNET_PROXYSETTINGS","mfidl/MFNET_PROXYSETTING_AUTO","mfidl/MFNET_PROXYSETTING_BROWSER","mfidl/MFNET_PROXYSETTING_MANUAL","mfidl/MFNET_PROXYSETTING_NONE"]
old-location: mf\mfnet_proxysettings.htm
tech.root: mf
ms.assetid: b9ec76bc-d8d1-4ba1-b6c4-02bcac9b53a0
ms.date: 12/05/2018
ms.keywords: MFNET_PROXYSETTINGS, MFNET_PROXYSETTINGS enumeration [Media Foundation], MFNET_PROXYSETTING_AUTO, MFNET_PROXYSETTING_BROWSER, MFNET_PROXYSETTING_MANUAL, MFNET_PROXYSETTING_NONE, b9ec76bc-d8d1-4ba1-b6c4-02bcac9b53a0, mf.mfnet_proxysettings, mfidl/MFNET_PROXYSETTINGS, mfidl/MFNET_PROXYSETTING_AUTO, mfidl/MFNET_PROXYSETTING_BROWSER, mfidl/MFNET_PROXYSETTING_MANUAL, mfidl/MFNET_PROXYSETTING_NONE
req.header: mfidl.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MFNET_PROXYSETTINGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFNET_PROXYSETTINGS
 - mfidl/_MFNET_PROXYSETTINGS
 - MFNET_PROXYSETTINGS
 - mfidl/MFNET_PROXYSETTINGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFNET_PROXYSETTINGS
---

# MFNET_PROXYSETTINGS enumeration


## -description

Specifies how the default proxy locator will specify the connection settings to a proxy server. The application must set these values in the <a href="/windows/desktop/medfound/mfnetsource-proxysettings-property">MFNETSOURCE_PROXYSETTINGS</a> property.

## -enum-fields

### -field MFNET_PROXYSETTING_NONE:0

The proxy locator bypasses all addresses.

### -field MFNET_PROXYSETTING_MANUAL:1

The proxy locator uses manual settings. The application must set the following properties:

<ul>
<li>
<a href="/windows/desktop/medfound/mfnetsource-proxyhostname-property">MFNETSOURCE_PROXYHOSTNAME</a>
</li>
<li>
<a href="/windows/desktop/medfound/mfnetsource-proxyport-property">MFNETSOURCE_PROXYPORT</a>
</li>
<li>
<a href="/windows/desktop/medfound/mfnetsource-proxybypassforlocal-property">MFNETSOURCE_PROXYBYPASSFORLOCAL</a>
</li>
<li>
<a href="/windows/desktop/medfound/mfnetsource-proxyexceptionlist-property">MFNETSOURCE_PROXYEXCEPTIONLIST</a>
</li>
</ul>

### -field MFNET_PROXYSETTING_AUTO:2

The proxy locator automatically discovers proxy servers by using the WinInet auto-proxy detection mechanism.

### -field MFNET_PROXYSETTING_BROWSER:3

The proxy locator uses the proxy settings of the browser. By default, the proxy locator sets this value for HTTP.

## -see-also

<a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator">MFCreateProxyLocator</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="/windows/desktop/medfound/proxy-support-for-network-sources">Proxy Support for Network Sources</a>
