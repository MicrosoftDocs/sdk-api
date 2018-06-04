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

# IWTSProtocolLicenseConnection::RequestLicensingCapabilities


## -description


<p class="CCE_Message">[<b>IWTSProtocolLicenseConnection::RequestLicensingCapabilities</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/a5814a01-9e4b-4510-b6a5-fa6edc6a15ed">IWRdsProtocolLicenseConnection::RequestLicensingCapabilities</a>.]

Requests license capabilities from the client.


## -parameters




### -param ppLicenseCapabilities




### -param pcbLicenseCapabilities [in, out]

A pointer to an integer that contains the size of the structure specified by the <i>ppLicensingCapabilities</i> parameter.


#### - ppLicensingCapabilities [out]

A pointer to a <a href="https://msdn.microsoft.com/975a534e-03f1-4c8f-9de1-42144e31c8cb">WTS_LICENSE_CAPABILITIES</a> structure that contains information about the client license capabilities.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. 




## -see-also




<a href="https://msdn.microsoft.com/3f6925b6-c712-40c6-8b48-7df8ef4a9872">IWTSProtocolLicenseConnection</a>
 

 

