---
UID: NF:dsgetdc.DsGetDcNextW
title: DsGetDcNextW function (dsgetdc.h)
description: Retrieves the next domain controller in a domain controller enumeration operation. (Unicode)
helpviewer_keywords: ["DsGetDcNext", "DsGetDcNext function [Active Directory]", "DsGetDcNextW", "ad.dsgetdcnext", "dsgetdc/DsGetDcNext", "dsgetdc/DsGetDcNextW"]
old-location: ad\dsgetdcnext.htm
tech.root: ad
ms.assetid: 2906772f-4391-411b-b0a9-5a20ebb6c0ee
ms.date: 12/05/2018
ms.keywords: DsGetDcNext, DsGetDcNext function [Active Directory], DsGetDcNextA, DsGetDcNextW, ad.dsgetdcnext, dsgetdc/DsGetDcNext, dsgetdc/DsGetDcNextA, dsgetdc/DsGetDcNextW
req.header: dsgetdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsGetDcNextW (Unicode) and DsGetDcNextA (ANSI)
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
 - DsGetDcNextW
 - dsgetdc/DsGetDcNextW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - DsGetDcNext
 - DsGetDcNextA
 - DsGetDcNextW
---

# DsGetDcNextW function


## -description

The <b>DsGetDcNext</b> function retrieves the next domain controller in a domain controller enumeration operation.

## -parameters

### -param GetDcContextHandle [in]

Contains the domain controller enumeration context handle provided by the <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcopena">DsGetDcOpen</a> function.

### -param SockAddressCount [out, optional]

Pointer to a <b>ULONG</b> value that receives the number of elements in the <i>SockAddresses</i> array.
        If this parameter is <b>NULL</b>, socket addresses are not retrieved.

### -param SockAddresses [out, optional]

Pointer to an array of <a href="/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a> structures that receives the socket address data for the domain controller. <i>SockAddressCount</i> receives the number of elements in this array.

All returned addresses will be of type <b>AF_INET</b> or <b>AF_INET6</b>.
        The <b>sin_port</b> member contains the port from the server record.
            A port of 0 indicates no port is available from DNS.

The caller must free this memory when it is no longer required by calling <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>.

This parameter is ignored if <i>SockAddressCount</i> is <b>NULL</b>.

### -param DnsHostName [out, optional]

Pointer to a string pointer that receives the DNS name of the domain controller.
        This parameter receives <b>NULL</b> if no host name is known. The caller must free this memory when it is no longer required by calling <a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a>.

## -returns

Returns <b>ERROR_SUCCESS</b> if successful or a Win32 or RPC error otherwise. Possible error values include the following.

## -remarks

To reset the enumeration, close the current enumeration by calling <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcclosew">DsGetDcClose</a> and then reopen the enumeration by calling <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcopena">DsGetDcOpen</a> again.

The DC returned by <b>DsGetDcNext</b> will not be a Read-only DC (RODC) because those DCs only register site-specific and CName records, and both <b>DsGetDcNext</b> and <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcopena">DsGetDcOpen</a> look for DNS SRV records.

The following procedure shows how to get a complete DC list from a computer running Windows Server 2008.

<p class="proch"><b>To obtain a complete list of domain controllers</b>

<ol>
<li>Use <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a> to get a domain controller name.</li>
<li>Use <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a> to connect to that domain controller.</li>
<li>Call <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsgetdomaincontrollerinfoa">DsGetDomainControllerInfo</a> with InfoLevel 3 (<b>DS_DOMAIN_CONTROLLER_INFO_3</b>) to get the complete list, including RODCs.</li>
</ol>




> [!NOTE]
> The dsgetdc.h header defines DsGetDcNext as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/AD/directory-service-functions">Directory Service Functions</a>



<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcclosew">DsGetDcClose</a>



<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcopena">DsGetDcOpen</a>



<a href="/windows/desktop/AD/enumerating-domain-controllers">Enumerating Domain Controllers</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>



<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a>
