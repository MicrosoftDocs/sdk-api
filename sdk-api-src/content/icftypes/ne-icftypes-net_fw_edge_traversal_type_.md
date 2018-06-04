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

# NET_FW_EDGE_TRAVERSAL_TYPE_ enumeration


## -description


The <b>NET_FW_EDGE_TRAVERSAL_TYPE</b> enumerated type specifies  the conditions under which edge traversal traffic is allowed.


## -enum-fields




### -field NET_FW_EDGE_TRAVERSAL_TYPE_DENY

Edge traversal traffic is always blocked.

This is the same as setting the EdgeTraversal property using <a href="https://msdn.microsoft.com/59e2a140-bf55-4f0e-bf4b-1a39d3dc0457">INetFwRule</a> to <b>VARIANT_FALSE</b>.


### -field NET_FW_EDGE_TRAVERSAL_TYPE_ALLOW

Edge traversal traffic is always allowed.

This is the same as setting the EdgeTraversal property using <a href="https://msdn.microsoft.com/59e2a140-bf55-4f0e-bf4b-1a39d3dc0457">INetFwRule</a> to <b>VARIANT_TRUE</b>.


### -field NET_FW_EDGE_TRAVERSAL_TYPE_DEFER_TO_APP

Edge traversal traffic is allowed when the application sets the <a href="https://msdn.microsoft.com/bfb934b3-1e86-431f-a21c-880048d32d35">IPV6_PROTECTION_LEVEL</a> socket option to <b>PROTECTION_LEVEL_UNRESTRICTED</b>. Otherwise, it is blocked.


### -field NET_FW_EDGE_TRAVERSAL_TYPE_DEFER_TO_USER

The user is prompted whether to allow edge traversal traffic when the application sets the IPV6_PROTECTION_LEVEL socket option to <b>PROTECTION_LEVEL_UNRESTRICTED</b>. If the user chooses to allow  edge traversal traffic, the rule is modified to defer to the application's settings.

If the application has not set the IPV6_PROTECTION_LEVEL socket option to <b>PROTECTION_LEVEL_UNRESTRICTED</b>, edge traversal traffic is blocked.

In order to use this option, the firewall rule must have both the application path and protocol scopes specified. This option cannot be used if port(s) are defined.


## -remarks



    In order for Windows Firewall to dynamically allow edge traversal traffic, the application must use the  <a href="https://msdn.microsoft.com/bfb934b3-1e86-431f-a21c-880048d32d35">IPV6_PROTECTION_LEVEL</a> socket option on the listening socket
        and set it to <b>PROTECTION_LEVEL_UNRESTRICTED</b> only in the cases where edge traversal traffic should be allowed. The Windows Firewall rule added for the application must then set 
            its edge traversal option  to <b>NET_FW_EDGE_TRAVERSAL_TYPE_DEFER_TO_APP</b> or <b>NET_FW_EDGE_TRAVERSAL_TYPE_DEFER_TO_USER</b>.




## -see-also




<a href="https://msdn.microsoft.com/59e2a140-bf55-4f0e-bf4b-1a39d3dc0457">INetFwRule</a>



<a href="https://msdn.microsoft.com/bfb934b3-1e86-431f-a21c-880048d32d35">IPV6_PROTECTION_LEVEL</a>



<a href="https://msdn.microsoft.com/72b85ab7-feb4-4bd2-8581-041e2c6d93b1">Windows Firewall with Advanced Security Enumerated Types</a>



<a href="https://msdn.microsoft.com/b1b154f1-2574-4e8e-a088-5e502bb889e7">Windows Firewall with Advanced Security Reference</a>
 

 

