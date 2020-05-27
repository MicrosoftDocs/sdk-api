---
UID: NF:dsgetdc.DsAddressToSiteNamesExW
title: DsAddressToSiteNamesExW function (dsgetdc.h)
description: Obtains the site and subnet names corresponding to the addresses specified.
helpviewer_keywords: ["DsAddressToSiteNamesEx","DsAddressToSiteNamesEx function [Active Directory]","DsAddressToSiteNamesExA","DsAddressToSiteNamesExW","ad.dsaddresstositenamesex","dsgetdc/DsAddressToSiteNamesEx","dsgetdc/DsAddressToSiteNamesExA","dsgetdc/DsAddressToSiteNamesExW"]
old-location: ad\dsaddresstositenamesex.htm
tech.root: ad
ms.assetid: 60ac6195-6e43-46da-a1e6-74ec989cd0c4
ms.date: 12/05/2018
ms.keywords: DsAddressToSiteNamesEx, DsAddressToSiteNamesEx function [Active Directory], DsAddressToSiteNamesExA, DsAddressToSiteNamesExW, ad.dsaddresstositenamesex, dsgetdc/DsAddressToSiteNamesEx, dsgetdc/DsAddressToSiteNamesExA, dsgetdc/DsAddressToSiteNamesExW
f1_keywords:
- dsgetdc/DsAddressToSiteNamesEx
dev_langs:
- c++
req.header: dsgetdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsAddressToSiteNamesExW (Unicode) and DsAddressToSiteNamesExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Netapi32.dll
api_name:
- DsAddressToSiteNamesEx
- DsAddressToSiteNamesExA
- DsAddressToSiteNamesExW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DsAddressToSiteNamesExW function


## -description


The <b>DsAddressToSiteNamesEx</b> function obtains  the site and subnet names corresponding to the addresses specified.


## -parameters




### -param ComputerName [in, optional]

Pointer to a null-terminated string that specifies the name of the remote server to process this function. This parameter must be the name of a domain controller. A non-domain controller can call this function by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a> to find the domain controller.


### -param EntryCount [in]

Contains the number of elements in the <i>SocketAddresses</i> array.


### -param SocketAddresses [in]

Contains an array of <a href="https://docs.microsoft.com/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a> structures that contain the addresses to convert. Each address in this array must be of the type <b>AF_INET</b>. <i>EntryCount</i> contains the number of elements in this array.


### -param SiteNames [out]

Receives an array of null-terminated string pointers that contain the site names for the addresses. Each element in this array corresponds to the same element in the <i>SocketAddresses</i> array. An element is <b>NULL</b> if the corresponding address does not map to any known site or if the address entry is not of the proper form. The caller must free this array when it is no longer required by calling <a href="https://docs.microsoft.com/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a>.


### -param SubnetNames [out]

Receives an array of null-terminated string pointers that contain the subnet names used to perform the address to site name mappings. Each element in this array corresponds to the same element in the <i>SocketAddresses</i> array. An element is <b>NULL</b> if the corresponding address to site name mapping was not determined or if no subnet was used to perform the
        corresponding address to site mapping. The latter will be the case when there is exactly
        one site in the enterprise with no subnet objects mapped to it. The caller must free this array when it is no longer required by calling <a href="https://docs.microsoft.com/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a>.


## -returns



Returns <b>NO_ERROR</b> if successful or a Win32 or RPC error otherwise. The following are possible error codes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/AD/directory-service-functions">Directory Service Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsgetdc/nf-dsgetdc-dsaddresstositenamesa">DsAddressToSiteNames</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a>
 

 

