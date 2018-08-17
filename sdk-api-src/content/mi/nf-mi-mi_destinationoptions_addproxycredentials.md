---
UID: NF:mi.MI_DestinationOptions_AddProxyCredentials
title: MI_DestinationOptions_AddProxyCredentials function
author: windows-sdk-content
description: Adds credentials to authenticate against a proxy.
old-location: wmi_v2\mi_destinationoptions_addproxycredentials.htm
old-project: wmi_v2
ms.assetid: 9cf3432d-145a-4252-95e3-f4c1866caf13
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: MI_DestinationOptions_AddProxyCredentials, MI_DestinationOptions_AddProxyCredentials function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_AddProxyCredentials, wmi_v2.mi_destinationoptions_addproxycredentials
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mi.h
req.include-header: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: MI_Type
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_DestinationOptions_AddProxyCredentials
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_DestinationOptions_AddProxyCredentials function


## -description


Adds credentials to authenticate against a proxy.


## -parameters




### -param options [in, out]

A pointer to a destination options structure.


### -param credentials [in]

Credentials used when communicating with the destination machine.


## -returns



This function returns MI_INLINE MI_Result.




## -remarks



Not all protocol transports support proxy configuration.  Not all proxy servers support all authentication types.  If the proxy requires dual-factor authentication this function can be called with both sets of credentials.



