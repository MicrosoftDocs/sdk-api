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

# NdrDllGetClassObject function


## -description


The <b>NdrDllGetClassObject</b> function retrieves the class object of the proxy or stub.


## -parameters




### -param rclsid [in]

Class identifier of the proxy or stub to retrieve.


### -param riid [in]

Interface identifier of the <a href="_com_ipsfactorybuffer">IPSFactoryBuffer</a> interface.


### -param ppv [out]

Address of the output variable that receives the interface pointer requested in <i>riid</i>.


### -param pProxyFileList [in]

Pointer to the <a href="https://msdn.microsoft.com/dbe797da-3ec3-4fe0-83bf-30669127a401">ProxyFileInfo</a> structure, which contains information about the proxy and stub.


### -param pclsid [in]

Pointer to the class identifier of the proxy or stub. Specify <i>pclsid</i> if the <b>PROXY_CLSID</b> constant is defined in the source code or as a C compiler option.


### -param pPSFactoryBuffer [in]

Pointer to the <a href="_com_ipsfactorybuffer">IPSFactoryBuffer</a> object.  The pointer is contained in the global variable, gPFactory, defined in RpcProxy.h.


## -returns



Returns S_OK on success.



