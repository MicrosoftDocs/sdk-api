---
UID: NF:netfw.INetFwRule.get_ServiceName
title: INetFwRule::get_ServiceName
author: windows-sdk-content
description: Specifies the service name property of the application.
old-location: ics\inetfwrule_servicename.htm
old-project: ics
ms.assetid: 52bcc317-b900-44b6-8ab4-637ffbd74729
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: INetFwRule interface [ICS/ICF],ServiceName property, INetFwRule.ServiceName, INetFwRule.get_ServiceName, INetFwRule::ServiceName, INetFwRule::get_ServiceName, INetFwRule::put_ServiceName, ServiceName property [ICS/ICF], ServiceName property [ICS/ICF],INetFwRule interface, get_ServiceName, ics.inetfwrule_servicename, netfw/INetFwRule::ServiceName, netfw/INetFwRule::get_ServiceName, netfw/INetFwRule::put_ServiceName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: netfw.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: NETISO_ERROR_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
api_name:
 - INetFwRule.ServiceName
 - INetFwRule.get_ServiceName
 - INetFwRule.put_ServiceName
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetFwRule::get_ServiceName


## -description


Specifies the service name property of the application.

This property is read/write.


## -parameters


## -remarks



This property is optional. A serviceName value of "*" indicates that a service, not an application,  must be sending or receiving traffic.

Also see the restrictions on changing properties described in the Remarks section of the <a href="https://msdn.microsoft.com/59e2a140-bf55-4f0e-bf4b-1a39d3dc0457">INetFwRule</a> interface page.




## -see-also




<a href="https://msdn.microsoft.com/59e2a140-bf55-4f0e-bf4b-1a39d3dc0457">INetFwRule</a>
 

 

