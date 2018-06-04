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

# LPDHCP_ENTRY_POINT_FUNC callback function


## -description


The 
<b>DhcpServerCalloutEntry</b> function is called by Microsoft DHCP Server to initialize a third-party DLL, and to discover for which events the third-party DLL wants notification. The 
<b>DhcpServerCalloutEntry</b> function is implemented by third-party DLLs.


## -parameters




### -param ChainDlls [in]

Collection of remaining third-party DLLs that provided registry entries requesting notification of DHCP Server events, in REG_MULTI_SZ format.


### -param CalloutVersion [in]

Version of the DHCP Server API that the third-party DLL is expected to support. The current version number is zero.


### -param CalloutTbl [out]

Cumulative set of notification hooks requested by all third-party DLLs, in the form of a 
<a href="https://msdn.microsoft.com/fa57e5c5-2335-44ba-8642-61dcb8b33ffe">DHCP_CALLOUT_TABLE</a> structure.


## -returns



Return values are defined by the application providing the callback.




## -remarks



Upon successful loading of a third-party DLL, Microsoft DHCP Server calls the DLL's 
<b>DhcpServerCalloutEntry</b> function. If this function call succeeds, Microsoft DHCP Server does not attempt to load any further third-party DLLs, and instead passes the list of remaining third-party DLLs in the <i>ChainDlls</i> parameter. It is the responsibility of the loaded third-party DLL to ensure that:

<ul>
<li>other third-party DLLs are loaded</li>
<li>their 
<b>DhcpServerCalloutEntry</b> function called</li>
<li>the merged list of requested notification entry points are returned to Microsoft DHCP Server in the <i>CalloutTbl</i> parameter.</li>
</ul>
The initially loaded third-party DLL is responsible for maintaining a table of cumulative notification entry points, and upon notification of a particular event, must call all chained third-party DLLs before returning to Microsoft DHCP Server.

<div class="alert"><b>Note</b>  For version negotiation, Microsoft DHCP Server may call the 
<b>DhcpServerCalloutEntry</b> function until a compatible version is found.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/782dd73a-7f32-4001-859b-21379f1e80d4">Chaining Multiple Third-Party DLLs</a>



<a href="https://msdn.microsoft.com/fa57e5c5-2335-44ba-8642-61dcb8b33ffe">DHCP_CALLOUT_TABLE</a>



<a href="https://msdn.microsoft.com/5fd828d6-4d62-4823-a2f1-15782b5cd28c">Registry Value Types</a>
 

 

