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

# IWTSProtocolLicenseConnection::RequestClientLicense


## -description


<p class="CCE_Message">[<b>IWTSProtocolLicenseConnection::RequestClientLicense</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/73660029-2d2e-4240-babe-208daa164290">IWRdsProtocolLicenseConnection::RequestClientLicense</a>.]

Requests a license from the client.


## -parameters




### -param Reserve1 [in]

A pointer to a byte array that contains additional data that can be acted upon by the client.


### -param Reserve2 [in]

An integer that contains the size, in bytes, of the data specified by the <i>Reserve1</i> parameter.


### -param ppClientLicense [out]

A pointer to a byte array that contains the license request.


### -param pcbClientLicense [in, out]

An integer that contains the size, in bytes, of the request specified by the <i>ppClientLicense</i> parameter.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



For more information about the byte arrays exchanged in this call, see <a href="http://go.microsoft.com/fwlink/p/?linkid=157338">[MS-RDPELE]: Remote Desktop Protocol: Licensing Extension</a>.




## -see-also




<a href="https://msdn.microsoft.com/3f6925b6-c712-40c6-8b48-7df8ef4a9872">IWTSProtocolLicenseConnection</a>
 

 

