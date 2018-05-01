---
UID: NF:dhcpsapi.DhcpServerQueryAttributes
title: DhcpServerQueryAttributes function
author: windows-driver-content
description: Returns an array of attributes set on the DHCP server.
old-location: dhcp\dhcpserverqueryattributes.htm
old-project: DHCP
ms.assetid: 24c3e7b2-80eb-4fee-aea6-38243d25c50b
ms.author: windowsdriverdev
ms.date: 4/7/2018
ms.keywords: DhcpServerQueryAttributes, DhcpServerQueryAttributes function [DHCP], dhcp.dhcpserverqueryattributes, dhcpsapi/DhcpServerQueryAttributes
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: QuarantineStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpsapi.dll
api_name:
-	DhcpServerQueryAttributes
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpServerQueryAttributes function


## -description



      The <b>DhcpServerQueryAttributes</b> function returns an array of attributes set on the DHCP server.


## -parameters




### -param ServerIpAddr [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param dwReserved [in]

Reserved. This value must be set to zero.


### -param dwAttribCount [in]

Specifies the number of attributes listed in <i>pDhcpAttribArr</i>.


### -param pDhcpAttribs [in]

Specifies an array of <a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_ATTRIB_ID</a> values (of length <i>dwAttribCount</i>) to retrieve the corresponding attribute information from.


### -param pDhcpAttribArr [out]

Pointer to a <a href="https://msdn.microsoft.com/2a9831ae-b0ba-4cec-b7a9-6e9d9bee82c5">DHCP_ATTRIB_ARRAY</a> structure that contains the attributes directly corresponding to the attribute ID values specified in <i>pDhcpAttribs[]</i>.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -remarks



A DHCP server attribute is a value that can be queried to determine supported and available features.

Callers of this function should free the memory pointed to by <i>pDhcpAttribs</i> and <i>pDhcpAttribArr</i> after use.




## -see-also




<a href="https://msdn.microsoft.com/2a9831ae-b0ba-4cec-b7a9-6e9d9bee82c5">DHCP_ATTRIB_ARRAY</a>



<a href="https://msdn.microsoft.com/8a522a8d-0b65-4dce-a785-d2b0c70e2794">DhcpServerQueryAttribute</a>
 

 

