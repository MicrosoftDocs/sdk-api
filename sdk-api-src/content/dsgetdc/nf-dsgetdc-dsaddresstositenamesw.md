---
UID: NF:dsgetdc.DsAddressToSiteNamesW
title: DsAddressToSiteNamesW function (dsgetdc.h)
description: Obtains the site names corresponding to the specified addresses. (Unicode)
helpviewer_keywords: ["DsAddressToSiteNames", "DsAddressToSiteNames function [Active Directory]", "DsAddressToSiteNamesW", "_glines_dsaddresstositenames", "ad.dsaddresstositenames", "dsgetdc/DsAddressToSiteNames", "dsgetdc/DsAddressToSiteNamesW"]
old-location: ad\dsaddresstositenames.htm
tech.root: ad
ms.assetid: 4d70dbee-be33-4d2a-a200-3696443fa853
ms.date: 12/05/2018
ms.keywords: DsAddressToSiteNames, DsAddressToSiteNames function [Active Directory], DsAddressToSiteNamesA, DsAddressToSiteNamesW, _glines_dsaddresstositenames, ad.dsaddresstositenames, dsgetdc/DsAddressToSiteNames, dsgetdc/DsAddressToSiteNamesA, dsgetdc/DsAddressToSiteNamesW
req.header: dsgetdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsAddressToSiteNamesW (Unicode) and DsAddressToSiteNamesA (ANSI)
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
 - DsAddressToSiteNamesW
 - dsgetdc/DsAddressToSiteNamesW
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
 - DsAddressToSiteNames
 - DsAddressToSiteNamesA
 - DsAddressToSiteNamesW
---

# DsAddressToSiteNamesW function


## -description

The <b>DsAddressToSiteNames</b> function obtains  the site names corresponding to the specified addresses.

## -parameters

### -param ComputerName [in, optional]

Pointer to a null-terminated string that specifies the name of the remote server to process this function. This parameter must be the name of a domain controller. A non-domain controller can call this function by calling 
<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a> to find the domain controller.

### -param EntryCount [in]

Contains the number of elements in the <i>SocketAddresses</i> array.

### -param SocketAddresses [in]

Contains an array of <a href="/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a> structures that contain the addresses to convert. Each address in this array must be of the type <b>AF_INET</b>. <i>EntryCount</i> contains the number of elements in this array.

### -param SiteNames [out]

Receives an array of null-terminated string pointers that contain the site names for the addresses. Each element in this array corresponds to the same element in the <i>SocketAddresses</i> array. An element is <b>NULL</b> if the corresponding address does not map to any known site or if the address entry is not of the proper form. The caller must free this array when it is no longer required by calling <a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a>.

## -returns

Returns <b>NO_ERROR</b> if successful or a Win32 or RPC error otherwise. The following list lists possible error codes.

## -see-also

<a href="/windows/desktop/AD/directory-service-functions">Directory Service Functions</a>



<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsaddresstositenamesexa">DsAddressToSiteNamesEx</a>



<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a>



<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a>

## -remarks

> [!NOTE]
> The dsgetdc.h header defines DsAddressToSiteNames as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
