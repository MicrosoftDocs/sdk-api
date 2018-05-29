---
UID: NF:netfw.NetworkIsolationGetEnterpriseIdAsync
title: NetworkIsolationGetEnterpriseIdAsync function
author: windows-sdk-content
description: Gets the Enterprise ID for Enterprise Data Protection Server endpoints.
old-location: ics\networkisolationgetenterpriseidasync.htm
old-project: ICS
ms.assetid: 709211F9-FE7A-4C43-AD35-101C4B64ED26
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: NetworkIsolationGetEnterpriseIdAsync, NetworkIsolationGetEnterpriseIdAsync function [ICS/ICF], ics.networkisolationgetenterpriseidasync, netfw/NetworkIsolationGetEnterpriseIdAsync
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NETISO_ERROR_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	firewallapi.dll
api_name:
-	NetworkIsolationGetEnterpriseIdAsync
product: Windows
targetos: Windows
req.lib: 
req.dll: Firewallapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NetworkIsolationGetEnterpriseIdAsync function


## -description


Gets the Enterprise ID for Enterprise Data Protection Server endpoints.


## -parameters




### -param wszServerName [in]

The name of the Enterprise Data Protection Server.


### -param dwFlags [in]

Not implemented. Set to 0.


### -param context [in, optional]

Optional context pointer. 


### -param callback [in]

Function pointer that will be invoked when a notification is ready for delivery.


### -param hOperation [out]

The handle for the Enterprise Data Protection Server endpoints.


## -returns



Returns ERROR_SUCCESS if successful, or an error value otherwise. 



