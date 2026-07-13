---
UID: NF:ntdsapi.DsBindW
title: DsBindW function (ntdsapi.h)
description: Binds to a domain controller. (Unicode)
helpviewer_keywords: ["DsBind", "DsBind function [Active Directory]", "DsBindW", "_glines_dsbind", "ad.dsbind", "ntdsapi/DsBind", "ntdsapi/DsBindW"]
old-location: ad\dsbind.htm
tech.root: ad
ms.assetid: c73cd16d-ccfd-4f61-b1c5-50130bef64d7
ms.date: 12/05/2018
ms.keywords: DsBind, DsBind function [Active Directory], DsBindA, DsBindW, _glines_dsbind, ad.dsbind, ntdsapi/DsBind, ntdsapi/DsBindA, ntdsapi/DsBindW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsBindW (Unicode) and DsBindA (ANSI)
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
 - DsBindW
 - ntdsapi/DsBindW
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
 - DsBind
 - DsBindA
 - DsBindW
---

# DsBindW function


## -description

The <b>DsBind</b> function binds to a domain controller.<b>DsBind</b> uses the default process credentials to bind to the domain controller. To specify alternate credentials, use the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a> function.

## -parameters

### -param DomainControllerName [in, optional]

Pointer to a null-terminated string that contains the name of the domain controller to bind to. This name can be the name of the domain controller or the fully qualified DNS name of the domain controller. Either name type can, optionally, be preceded by two backslash characters. All of the following examples represent correctly formatted domain controller names:

<ul>
<li>"FAB-DC-01"</li>
<li>"\\FAB-DC-01"</li>
<li>"FAB-DC-01.fabrikam.com"</li>
<li>"\\FAB-DC-01.fabrikam.com"</li>
</ul>
This parameter can be <b>NULL</b>. For more information, see Remarks.

### -param DnsDomainName [in, optional]

Pointer to a null-terminated string that contains the fully qualified DNS name of the domain to bind to. This parameter can be <b>NULL</b>. For more  information, see Remarks.

### -param phDS [out]

Address of a <b>HANDLE</b> value that receives the binding handle. To close this handle, pass it to the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnBind</a> function.

## -returns

Returns <b>ERROR_SUCCESS</b> if successful or a Windows or RPC error code otherwise. The following are the most common error codes.

## -remarks

The behavior of the 
    <b>DsBind</b> function is determined by the contents of the <i>DomainControllerName</i> and <i>DnsDomainName</i> parameters. The following list describes the behavior of this function based on the contents of these parameters.

<table>
<tr>
<th><i>DomainControllerName</i></th>
<th><i>DnsDomainName</i></th>
<th>Description</th>
</tr>
<tr>
<td>
<b>NULL</b>

</td>
<td>
<b>NULL</b>

</td>
<td>
<b>DsBind</b> will attempt to bind to a global catalog server in the forest of the local computer.

</td>
</tr>
<tr>
<td>
(value)

</td>
<td>
<b>NULL</b>

</td>
<td>
<b>DsBind</b> will attempt to bind to the domain controller specified by the  <i>DomainControllerName</i> parameter.

</td>
</tr>
<tr>
<td>
<b>NULL</b>

</td>
<td>
(value)

</td>
<td>
<b>DsBind</b> will attempt to bind to any domain controller in the domain specified by <i>DnsDomainName</i> parameter.

</td>
</tr>
<tr>
<td>
(value</p>)</td>
<td>
(value)

</td>
<td>
The <i>DomainControllerName</i> parameter takes precedence. <b>DsBind</b> will attempt to bind to the domain controller specified by the  <i>DomainControllerName</i> parameter.

</td>
</tr>
</table>
 





> [!NOTE]
> The ntdsapi.h header defines DsBind as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/dsgetdc/ns-dsgetdc-domain_controller_infoa">DOMAIN_CONTROLLER_INFO</a>



<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>



<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsunbinda">DsUnBind</a>
