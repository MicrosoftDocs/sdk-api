---
UID: NF:ondemandconnroutehelper.FreeInterfaceContextTable
title: FreeInterfaceContextTable function (ondemandconnroutehelper.h)
description: This function frees the interface context table retrieved using the GetInterfaceContextTableForHostName function.
helpviewer_keywords: ["FreeInterfaceContextTable","FreeInterfaceContextTable function [Network Awareness]","nla.freeinterfacecontexttable","ondemandconnroutehelper/FreeInterfaceContextTable"]
old-location: nla\freeinterfacecontexttable.htm
tech.root: nla
ms.assetid: 79623E67-C255-498D-ACDA-8BC2AE925224
ms.date: 12/05/2018
ms.keywords: FreeInterfaceContextTable, FreeInterfaceContextTable function [Network Awareness], nla.freeinterfacecontexttable, ondemandconnroutehelper/FreeInterfaceContextTable
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
req.lib: OnDemandConnRouteHelper.lib
req.dll: OnDemandConnRouteHelper.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FreeInterfaceContextTable
 - ondemandconnroutehelper/FreeInterfaceContextTable
dev_langs:
 - c++
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
---

# FreeInterfaceContextTable function


## -description

This function frees the interface context table retrieved using the <a href="/windows/desktop/api/ondemandconnroutehelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname">GetInterfaceContextTableForHostName</a> function.

## -parameters

### -param InterfaceContextTable [in]

The interface context table retrieved using the <a href="/windows/desktop/api/ondemandconnroutehelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname">GetInterfaceContextTableForHostName</a> function.

## -see-also

<a href="/windows/desktop/api/ondemandconnroutehelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname">GetInterfaceContextTableForHostName</a>