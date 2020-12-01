---
UID: NF:ntdsapi.DsFreePasswordCredentials
title: DsFreePasswordCredentials function (ntdsapi.h)
description: Frees memory allocated for a credentials structure by the DsMakePasswordCredentials function.
helpviewer_keywords: ["DsFreePasswordCredentials","DsFreePasswordCredentials function [Active Directory]","_glines_dsfreepasswordcredentials","ad.dsfreepasswordcredentials","ntdsapi/DsFreePasswordCredentials"]
old-location: ad\dsfreepasswordcredentials.htm
tech.root: ad
ms.assetid: 3d008aa8-feff-426f-911b-a447257076c2
ms.date: 12/05/2018
ms.keywords: DsFreePasswordCredentials, DsFreePasswordCredentials function [Active Directory], _glines_dsfreepasswordcredentials, ad.dsfreepasswordcredentials, ntdsapi/DsFreePasswordCredentials
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
 - DsFreePasswordCredentials
 - ntdsapi/DsFreePasswordCredentials
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
 - API-MS-Win-Security-ActiveDirectoryClient-l1-1-0.dll
 - KernelBase.dll
 - API-Ms-Win-Security-ActiveDirectoryClient-L1-1-1.dll
api_name:
 - DsFreePasswordCredentials
---

# DsFreePasswordCredentials function


## -description

The <b>DsFreePasswordCredentials</b> function frees memory allocated for a credentials structure by the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsmakepasswordcredentialsa">DsMakePasswordCredentials</a> function.

## -parameters

### -param AuthIdentity [in]

Handle of the credential structure to be freed.

## -returns

This function does not return a value.

## -remarks

When the handle  in <i>AuthIdentity</i> is passed to <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>, <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnbind</a> must be called before freeing this handle. The normal sequence of events is:

<ol>
<li>Call <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsmakepasswordcredentialsa">DsMakePasswordCredentials</a> to obtain the credential handle.</li>
<li>Call <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>, passing the credential handle.</li>
<li>Call <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnbind</a> when the RPC connection is no longer required.</li>
<li>Call <b>DsFreePasswordCredentials</b> to free the credential handle.</li>
</ol>

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsmakepasswordcredentialsa">DsMakePasswordCredentials</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnbind</a>