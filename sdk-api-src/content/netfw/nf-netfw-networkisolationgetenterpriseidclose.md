---
UID: NF:netfw.NetworkIsolationGetEnterpriseIdClose
title: NetworkIsolationGetEnterpriseIdClose function
author: windows-sdk-content
description: This API is used for closing the handle returned by NetworkIsolationGetEnterpriseIdAsync as well as for synchronizing the operation.
old-location: ics\networkisolationgetenterpriseidclose.htm
tech.root: ics
ms.assetid: 85FE7431-CC20-4CD2-9853-9B81BB8B7160
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NetworkIsolationGetEnterpriseIdClose, NetworkIsolationGetEnterpriseIdClose function [ICS/ICF], ics.networkisolationgetenterpriseidclose, netfw/NetworkIsolationGetEnterpriseIdClose
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
req.lib: 
req.dll: Firewallapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - firewallapi.dll
api_name:
 - NetworkIsolationGetEnterpriseIdClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetworkIsolationGetEnterpriseIdClose function


## -description


This API is used for closing the handle returned by  <a href="https://msdn.microsoft.com/709211F9-FE7A-4C43-AD35-101C4B64ED26">NetworkIsolationGetEnterpriseIdAsync</a> as well as for synchronizing the operation.


## -parameters




### -param hOperation [in]

The handle to release.


### -param bWaitForOperation [in]

Indicates whether to wait for synchronization.


## -returns



Returns ERROR_SUCCESS if successful, or an error value otherwise. 



