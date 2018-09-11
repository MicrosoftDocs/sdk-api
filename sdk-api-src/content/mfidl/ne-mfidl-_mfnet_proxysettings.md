---
UID: NE:mfidl._MFNET_PROXYSETTINGS
title: "_MFNET_PROXYSETTINGS"
author: windows-sdk-content
description: Specifies how the default proxy locator will specify the connection settings to a proxy server.
old-location: mf\mfnet_proxysettings.htm
tech.root: medfound
ms.assetid: b9ec76bc-d8d1-4ba1-b6c4-02bcac9b53a0
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: MFNET_PROXYSETTINGS, MFNET_PROXYSETTINGS enumeration [Media Foundation], MFNET_PROXYSETTING_AUTO, MFNET_PROXYSETTING_BROWSER, MFNET_PROXYSETTING_MANUAL, MFNET_PROXYSETTING_NONE, _MFNET_PROXYSETTINGS, b9ec76bc-d8d1-4ba1-b6c4-02bcac9b53a0, mf.mfnet_proxysettings, mfidl/MFNET_PROXYSETTINGS, mfidl/MFNET_PROXYSETTING_AUTO, mfidl/MFNET_PROXYSETTING_BROWSER, mfidl/MFNET_PROXYSETTING_MANUAL, mfidl/MFNET_PROXYSETTING_NONE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFNET_PROXYSETTINGS
product: Windows
targetos: Windows
req.typenames: MFNET_PROXYSETTINGS
req.redist: 
---

# _MFNET_PROXYSETTINGS enumeration


## -description


Specifies how the default proxy locator will specify the connection settings to a proxy server. The application must set these values in the <a href="https://msdn.microsoft.com/85f2bd02-8a2f-46b5-b765-1a0bc5b6ccc3">MFNETSOURCE_PROXYSETTINGS</a> property.


## -enum-fields




### -field MFNET_PROXYSETTING_NONE

The proxy locator bypasses all addresses.
          


### -field MFNET_PROXYSETTING_MANUAL

The proxy locator uses manual settings. The application must set the following properties:

<ul>
<li>
<a href="https://msdn.microsoft.com/e53c86e9-c326-41c9-aa86-c80a750b9ce3">MFNETSOURCE_PROXYHOSTNAME</a>
</li>
<li>
<a href="https://msdn.microsoft.com/cd84911b-3658-489f-b454-23eded0cbfa0">MFNETSOURCE_PROXYPORT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/384343f5-5919-44da-b8ea-0c994b4743a8">MFNETSOURCE_PROXYBYPASSFORLOCAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/218883c5-9a26-4733-8308-1827cf1f2cd7">MFNETSOURCE_PROXYEXCEPTIONLIST</a>
</li>
</ul>

### -field MFNET_PROXYSETTING_AUTO

The proxy locator automatically discovers proxy servers by using the WinInet auto-proxy detection mechanism.
          


### -field MFNET_PROXYSETTING_BROWSER

The proxy locator uses the proxy settings of the browser. By default, the proxy locator sets this value for HTTP.
          


## -see-also




<a href="https://msdn.microsoft.com/9ad707df-533a-407b-a611-49bfb019affc">MFCreateProxyLocator</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/e739746d-2a09-4237-a7c1-0aed4e4516d7">Proxy Support for Network Sources</a>
 

 

