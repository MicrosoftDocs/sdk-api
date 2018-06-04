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

# DhcpEnumServers function


## -description



      The <b>DhcpEnumServers</b> function returns an enumerated list of DHCP servers found in the directory service.  


## -parameters




### -param Flags [in]

Reserved for future use. This field should be set to 0.


### -param IdInfo [in]

Pointer to an address containing the server's ID block. This field should be set to null.


### -param Servers [out]

Pointer to a <a href="https://msdn.microsoft.com/0f5fe4f3-4eaa-498b-ab48-bfb5ee8f5527">DHCP_SERVER_INFO_ARRAY</a>
       structure that contains the output list of DHCP servers.


### -param CallbackFn [in]

Pointer to the callback function that will be called when the server add operation completes. This field should be null.


### -param CallbackData [in]

Pointer to a data block containing the formatted structure for callback information. This field should be null.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/0f5fe4f3-4eaa-498b-ab48-bfb5ee8f5527">DHCP_SERVER_INFO_ARRAY</a>
 

 

