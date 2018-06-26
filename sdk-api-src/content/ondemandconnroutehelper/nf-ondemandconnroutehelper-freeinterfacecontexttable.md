---
UID: NF:ondemandconnroutehelper.FreeInterfaceContextTable
title: FreeInterfaceContextTable function
author: windows-sdk-content
description: This function frees the interface context table retrieved using the GetInterfaceContextTableForHostName function.
old-location: nla\freeinterfacecontexttable.htm
old-project: NLA
ms.assetid: 79623E67-C255-498D-ACDA-8BC2AE925224
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: FreeInterfaceContextTable, FreeInterfaceContextTable function [Network Awareness], nla.freeinterfacecontexttable, ondemandconnroutehelper/FreeInterfaceContextTable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ondemandconnroutehelper.h
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
tech.root: 
req.typenames: OLEVERB, *LPOLEVERB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OnDemandConnRouteHelper.dll
 - API-Ms-Win-Networking-InterfaceContexts-L1-1-0.dll
api_name:
 - FreeInterfaceContextTable
product: Windows
targetos: Windows
req.lib: OnDemandConnRouteHelper.lib
req.dll: OnDemandConnRouteHelper.dll
req.irql: 
req.product: ADAM
---

# FreeInterfaceContextTable function


## -description


This function frees the interface context table retrieved using the <a href="https://msdn.microsoft.com/BD687853-6242-4A72-BACE-13B681FD4674">GetInterfaceContextTableForHostName</a> function.


## -parameters




### -param InterfaceContextTable [in]

The interface context table retrieved using the <a href="https://msdn.microsoft.com/BD687853-6242-4A72-BACE-13B681FD4674">GetInterfaceContextTableForHostName</a> function.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/BD687853-6242-4A72-BACE-13B681FD4674">GetInterfaceContextTableForHostName</a>
 

 

