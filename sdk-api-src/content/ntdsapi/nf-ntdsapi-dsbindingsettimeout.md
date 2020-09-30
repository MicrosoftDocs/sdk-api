---
UID: NF:ntdsapi.DsBindingSetTimeout
title: DsBindingSetTimeout function (ntdsapi.h)
description: The DsBindingSetTimeout function sets the timeout value that is honored by all RPC calls that use the specified binding handle. RPC calls that required more time than the timeout value are canceled.
helpviewer_keywords: ["DsBindingSetTimeout","DsBindingSetTimeout function [Active Directory]","ad.dsbindingsettimeout","ntdsapi/DsBindingSetTimeout"]
old-location: ad\dsbindingsettimeout.htm
tech.root: ad
ms.assetid: abdaae89-fba3-4949-92a9-acd62898ec24
ms.date: 12/05/2018
ms.keywords: DsBindingSetTimeout, DsBindingSetTimeout function [Active Directory], ad.dsbindingsettimeout, ntdsapi/DsBindingSetTimeout
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsBindingSetTimeout
 - ntdsapi/DsBindingSetTimeout
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsBindingSetTimeout
---

# DsBindingSetTimeout function


## -description

The <b>DsBindingSetTimeout</b> function sets the timeout value
that is honored by all RPC calls that use the specified binding
handle. RPC calls that required more time than the timeout value are canceled.

## -parameters

### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.

### -param cTimeoutSecs [in]

Contains the new timeout value, in seconds.

## -returns

Returns <b>ERROR_SUCCESS</b> if successful or a Win32 or RPC error code otherwise. The following is a  possible error code.

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>