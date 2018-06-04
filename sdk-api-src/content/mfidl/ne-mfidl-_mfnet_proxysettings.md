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
 

 

