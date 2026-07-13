---
UID: NF:ntdsapi.DsRemoveDsServerA
title: DsRemoveDsServerA function (ntdsapi.h)
description: The DsRemoveDsServer function removes all traces of a directory service agent (DSA) from the global area of the directory service. (ANSI)
helpviewer_keywords: ["DsRemoveDsServerA", "ntdsapi/DsRemoveDsServerA"]
old-location: ad\dsremovedsserver.htm
tech.root: ad
ms.assetid: a79a2b71-10c7-495b-861f-0c7a4d86f720
ms.date: 12/05/2018
ms.keywords: DsRemoveDsServer, DsRemoveDsServer function [Active Directory], DsRemoveDsServerA, DsRemoveDsServerW, _glines_dsremovedsserver, ad.dsremovedsserver, ntdsapi/DsRemoveDsServer, ntdsapi/DsRemoveDsServerA, ntdsapi/DsRemoveDsServerW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsRemoveDsServerW (Unicode) and DsRemoveDsServerA (ANSI)
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
 - DsRemoveDsServerA
 - ntdsapi/DsRemoveDsServerA
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
 - DsRemoveDsServer
 - DsRemoveDsServerA
 - DsRemoveDsServerW
---

# DsRemoveDsServerA function


## -description

The <b>DsRemoveDsServer</b> function removes all traces of a directory service agent (DSA) from the global area of the directory service.

## -parameters

### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.

### -param ServerDN [in]

Pointer to a null-terminated string that specifies the fully qualified distinguished name of the domain controller to remove.

### -param DomainDN [in, optional]

Pointer to a null-terminated string that specifies a domain hosted by <i>ServerDN</i>. If this parameter is <b>NULL</b>, no verification is performed to ensure that <i>ServerDN</i> is the last domain controller in <i>DomainDN</i>.

### -param fLastDcInDomain [out, optional]

Pointer to a Boolean value that receives <b>TRUE</b> if <i>ServerDN</i> is the last DC in <i>DomainDN</i> or <b>FALSE</b> otherwise. This parameter receives <b>FALSE</b> if <i>DomainDN</i> is <b>NULL</b>.

### -param fCommit [in]

Contains a Boolean value that specifies if the domain controller should actually be removed. If this parameter is nonzero, <i>ServerDN</i> is removed. If this parameter is zero, the existence of <i>ServerDN</i> is checked and <i>fLastDcInDomain</i> is written, but the domain controller is not removed.

## -returns

Returns <b>ERROR_SUCCESS</b> if successful  or a Win32 or RPC error code if unsuccessful. Possible error codes include the following.

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsremovedsdomaina">DsRemoveDsDomain</a>

## -remarks

> [!NOTE]
> The ntdsapi.h header defines DsRemoveDsServer as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
