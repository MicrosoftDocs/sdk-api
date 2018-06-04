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

# IWMClientConnections2::GetClientInfo


## -description



The <b>GetClientInfo</b> method retrieves information about a client attached to a writer network sink.




## -parameters




### -param dwClientNum [in]

<b>DWORD</b> containing the client number.


### -param pwszNetworkAddress [out]

Pointer to a wide-character <b>null</b>-terminated string containing the network address of the client. Pass <b>NULL</b> to retrieve the size of the string, which is returned in <i>pcchNetworkAddress</i>.


### -param pcchNetworkAddress [in, out]

Pointer to a <b>DWORD</b> containing the size of <i>pwszNetworkAddress</i>, in wide characters. This size includes the terminating <b>null</b> character.


### -param pwszPort [out]

Pointer to a wide-character <b>null</b>-terminated string containing the network port of the client. Pass <b>NULL</b> to retrieve the size of the string, which is returned in <i>pcchPort</i>.


### -param pcchPort [in, out]

Pointer to a <b>DWORD</b> containing the size of <i>pwszPort</i>, in wide characters. This size includes the terminating <b>null</b> character.


### -param pwszDNSName [out]

Pointer to a wide-character <b>null</b>-terminated string containing the name of the domain name server supporting the client. Pass <b>NULL</b> to retrieve the size of the string, which is returned in <i>pcchDNSName</i>.


### -param pcchDNSName [in, out]

Pointer to a <b>DWORD</b> containing the size of <i>pwszDNSName</i>, in wide characters. This size includes the terminating <b>null</b> character.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7148dd13-e5de-4adb-89e7-3f02a463c2d1">IWMClientConnections2 Interface</a>
 

 

