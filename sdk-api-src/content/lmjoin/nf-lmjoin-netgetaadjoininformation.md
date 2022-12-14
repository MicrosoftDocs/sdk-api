---
UID: NF:lmjoin.NetGetAadJoinInformation
title: NetGetAadJoinInformation function (lmjoin.h)
description: Retrieves the join information for the specified tenant. This function examines the join information for Microsoft Azure Active Directory and the work account that the current user added.
helpviewer_keywords: ["NetGetAadJoinInformation","NetGetAadJoinInformation function [Network Management]","lmjoin/NetGetAadJoinInformation","netmgmt.netgetaadjoininformation"]
old-location: netmgmt\netgetaadjoininformation.htm
tech.root: NetMgmt
ms.assetid: C63B3AA7-FC7E-4CB9-9318-BD25560591AB
ms.date: 12/05/2018
ms.keywords: NetGetAadJoinInformation, NetGetAadJoinInformation function [Network Management], lmjoin/NetGetAadJoinInformation, netmgmt.netgetaadjoininformation
req.header: lmjoin.h
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetGetAadJoinInformation
 - lmjoin/NetGetAadJoinInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - netapi32.dll
api_name:
 - NetGetAadJoinInformation
---

# NetGetAadJoinInformation function


## -description

Retrieves the join information for the specified tenant. This function examines the join information for Microsoft Azure Active Directory and the work account that the current user added.

## -parameters

### -param pcszTenantId [in, optional]

The tenant identifier for the joined account. If the device
                       is not joined to Azure Active Directory (Azure AD), and the user currently logged into Windows added no Azure AD work accounts  for the specified tenant,
                       the buffer that the <i>ppJoinInfo</i> parameter points to  is set to NULL.

If the specified
                       tenant ID is NULL or empty, <i>ppJoinInfo</i> is set to the default
                       join account information, or NULL if the device is not joined to Azure AD and the current user added  no Azure AD work accounts.
                       
The default join account is one of the following:

<ul>
<li>The Azure AD account, if the device is joined to Azure AD.</li>
<li>The Azure AD work account that the current user added, if the device is not joined to Azure AD,
                       but the current user added a single Azure AD work account.</li>
<li>Any of the Azure AD work accounts that the current user added,  if the device is not joined to Azure AD, but the current user added multiple
                       Azure AD work accounts. The algorithm for selecting one of the work
                       accounts is not specified.</li>
</ul>

### -param ppJoinInfo [out]

The join information for the tenant that the <i>pcszTenantId</i> parameter specifies. If this parameter is NULL,  the device is not joined to Azure AD and the current user added no Azure AD work accounts. You must call
                     the <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netfreeaadjoininformation">NetFreeAadJoinInformation</a> function to free the memory allocated for
                     this structure.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netfreeaadjoininformation">NetFreeAadJoinInformation</a>