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

# DhcpServerQueryAttribute function


## -description


The <b>DhcpServerQueryAttribute</b> function returns specific attribute information from the DHCP server.


## -parameters




### -param ServerIpAddr [in]

Unicode string that contains the IP address of the DHCP server.


### -param dwReserved [in]

Reserved. This value must be zero.


### -param DhcpAttribId [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_ATTRIB_ID</a> value that specifies the particular DHCP server attribute to retrieve.


### -param pDhcpAttrib [out]

Pointer to a <a href="https://msdn.microsoft.com/26822137-8633-4e18-a69f-eeebf9e78f9a">DHCP_ATTRIB</a> structure that contains the location and type of the queried DHCP server attribute.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -remarks



A DHCP server attribute is a value that can be queried to determine supported and available features.

Callers of this function should free the memory pointed to by <i>pDhcpAttrib</i> after use.




## -see-also




<a href="https://msdn.microsoft.com/26822137-8633-4e18-a69f-eeebf9e78f9a">DHCP_ATTRIB</a>



<a href="https://msdn.microsoft.com/24c3e7b2-80eb-4fee-aea6-38243d25c50b">DhcpServerQueryAttributes</a>
 

 

