---
UID: NF:dhcpsapi.DhcpServerQueryAttribute
title: DhcpServerQueryAttribute function
author: windows-sdk-content
description: Returns specific attribute information from the DHCP server.
old-location: dhcp\dhcpserverqueryattribute.htm
old-project: DHCP
ms.assetid: 8a522a8d-0b65-4dce-a785-d2b0c70e2794
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: DhcpServerQueryAttribute, DhcpServerQueryAttribute function [DHCP], dhcp.dhcpserverqueryattribute, dhcpsapi/DhcpServerQueryAttribute
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: QuarantineStatus
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpServerQueryAttribute
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
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
 

 

