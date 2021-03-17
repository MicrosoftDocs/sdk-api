---
UID: NC:resapi.PSET_RESOURCE_LOCKED_MODE_ROUTINE
title: PSET_RESOURCE_LOCKED_MODE_ROUTINE (resapi.h)
description: Reports that locked mode was configured for a resource.
helpviewer_keywords: ["PSET_RESOURCE_LOCKED_MODE_ROUTINE","PSET_RESOURCE_LOCKED_MODE_ROUTINE callback function [Failover Cluster]","SetResourceLockedMode","SetResourceLockedMode callback","SetResourceLockedMode callback function [Failover Cluster]","mscs.setresourcelockedmode","resapi/PSET_RESOURCE_LOCKED_MODE_ROUTINE","resapi/SetResourceLockedMode"]
old-location: mscs\setresourcelockedmode.htm
tech.root: MsCS
ms.assetid: 000D127C-7BDE-4FC1-984E-2EE805E603FC
ms.date: 12/05/2018
ms.keywords: PSET_RESOURCE_LOCKED_MODE_ROUTINE, PSET_RESOURCE_LOCKED_MODE_ROUTINE callback function [Failover Cluster], SetResourceLockedMode, SetResourceLockedMode callback, SetResourceLockedMode callback function [Failover Cluster], mscs.setresourcelockedmode, resapi/PSET_RESOURCE_LOCKED_MODE_ROUTINE, resapi/SetResourceLockedMode
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSET_RESOURCE_LOCKED_MODE_ROUTINE
 - resapi/PSET_RESOURCE_LOCKED_MODE_ROUTINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - SetResourceLockedMode
---

# PSET_RESOURCE_LOCKED_MODE_ROUTINE callback function


## -description

Reports that  locked mode was configured for a resource.

## -parameters

### -param ResourceHandle [in]

A handle to the resource to configure.

### -param LockedModeEnabled [in]

<b>TRUE</b> to enable locked mode; otherwise <b>FALSE</b>.

### -param LockedModeReason [in]

A flag that specifies the reason that locked mode was configured.

## -returns

Returns <b>ERROR_SUCCESS</b> (0), if the operation succeeds; otherwise returns a system error code.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-dll-callback-functions">Resource DLL Callback Functions</a>